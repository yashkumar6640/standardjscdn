# standard.js
A CDN for standardjs(A Javascript framework)
<hr>
<h2>Application Structure:</h3><br>
<pre>
/app
    /components
              /home
                  /home.js
                  /home.html
                  /home.css
              /view
                  /view.js
                  /view.html
                  /view.css
/index.html
</pre>
<br>
<h3>Quick start example:</h3><br>
<b>index.html</b>

`<li><a data-standard-component="home">home</a></li>`

`<li><a data-standard-component="view">view</a></li>`<br><br>
 `<div class="container" standard-view></div>`
<br>

<b>home.html</b><br><br>
`<button id="homeId">Check Event</button> `<br><br>
<b>home.js</b>

<pre>
function log() {
  console.log("inside home called by check event button");
}
standard.storeComponent("home", {
  data: { title: "home page" },
  events: [
    {
      target: "#homeId",
      onClick: function() {
        console.log("in home click");
        console.log(this);
        log();
      }
    }
  ]
});
</pre>

<b>view.html</b><br><br>
`<button id="viewId">Check Event</button> `<br><br>
<b>view.js</b>

<pre>
function log() {
  console.log("inside view called by check event button");
}
standard.storeComponent("home", {
  data: { title: "home page" },
  events: [
    {
      target: "#viewId",
      onClick: function() {
        console.log("in view click");
        console.log(this);
        log();
      }
    }
  ]
});
</pre>

<h2>How to run:</h2>
Run your index.html with live server.
Include the standardjs file in script tag.

