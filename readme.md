This repo is a collection of examples illustrating how to use phantomJS to pre-render javascript pages on the server the purposes of Serch engine optomization. [This](http://thedigitalself.com/blog/seo-and-javascript-with-phantomjs-server-side-rendering) blog post describes the general concept. 

Basic

This is a very simple example using a nodejs server and a trivial abount of javascript to show off the gist of the concept. In this example, the index.html displas a simple message. This page is passed to a PhantomJS script via a nodeJs static server. The node server can be initialized with pre-rendering enabled or disabled. When pre-rendering is disabled viewing the source (not the element inspector), will reveal an empty "<h1>" tag even though the message is displayed. Ehen pre-rendering is enabled, viewing the source will reveal that the "<h1>" tag has a value equal to the javascript assignment. If you were a search engine spider, that "<h1>" would look like it was part of a static page and not dynamic javascript.

Starting the server with pre-rendering disabled.

$ node server.js 8888 false


Starting the server with pre-rendering enabled.

$ node server.js 8888 true