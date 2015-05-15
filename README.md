# nodecodingtest
Node Coding Test

# Javascript coding test

Please implement the following. There is no time limit or other restrictions apart from the mentioned.

1. Without using Javascript's `bind` function, implement the `magic` function so that:

  ```js
  var add = function(a, b) { return a + b; }
  var addTo = add.magic(2);

  var say = function(something) { return something; }
  var welcome = say.magic('Hi, how are you?');

  addTo(5) == 7;
  welcome() == 'Hi, how are you?';
  ```

2. Say you have a `http://basketball.example.com/thisweek.json` HTTP endpoint that returns the following JSON:

  ```json
  {
    "week": "51st of 2011",
    "games": [
      { "url": "http://basketball.example.com/game/1" },
      { "url": "http://basketball.example.com/game/2" },
      { "url": "http://basketball.example.com/game/3" },
      { "url": "http://basketball.example.com/game/4" }
    ]
  }
  ```

  The games entry is dynamic and may include arbitrary URL’s.
  Each of the URL endpoints returns some game data:

  ```json
  {
    "id": "1",
    "teams": [
      {
        "name": "Lakers",
        "score": 79
      },
      {
        "name": "Bulls",
        "score": 99
      }
    ]
  }
  ```

  Given that jQuery is available and loaded, write a summary function that prints a list of all scores formatted like `Lakers 79 - 99 Bulls`.

3. Write a function that creates a deep copy of an object, without using `JSON.stringify`.

4. Given the following `tab-panel.html`:

  ```html
  <html>
    <head>
      <link href="tab-panel.css" rel='stylesheet' type='text/css'></link>
    </head>
    <body>
    	<section>
    		<h2>Tab Panel One</h2>
    		<article title="Tab One">
    			<h3>Tab One</h3>
    			<p>Panel One - tab One</p>
    		</article>

    		<article title="Tab Two">
    			<h3>Tab Two</h3>
    			<p>Panel One - tab Two</p>
    		</article>
    	</section>
    	<section>
    		<h2>Tab Panel Two</h2>
    		<article title="Tab One">
    			<h3>Tab One</h3>
    			<p>Panel Two - Tab One</p>
    		</article>

    		<article title="Tab Two">
    			<h3>Tab Two</h3>
    			<p>Panel Two - tab Two</p>
    		</article>
    	</section>
    	<script src="tab-panel.js" type='text/javascript'></script>
    </body>
  </html>
  ```

  And the following `tab-panel.js` part:

  ```js
  var tabDemo = function() {
  	for(var i = 0; i < document.body.children.length; i++) {
  		child = document.body.children[i];
  		if(child.tagName.toLowerCase() != 'section') continue;

  		t = new TabPanel();
  		t.init(child);
  		window.panels.push(t);
  	}
  };
  var panels = [];
  window.onload = tabDemo;
  ```

  Without using jQuery, implement the `TabPanel` component that handles tabs switching. Add any applicable stylings to `tab-panel.css` (we aren't assessing artistry abilities - we are just after clean functional css).
