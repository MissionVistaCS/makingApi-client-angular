# Making API - Client w/ Angular
This tutorial goes with Aaroh's [makingApi-server](https://github.com/aarohmankad/makingApi-server). You can also see how to achieve the same thing with jQuery in [makingApi-client](https://github.com/aarohmankad/makingApi-client).  

1. Because our project will be making requests to a server, we'll need a very basic server to send static HTML/JS files. First create a package.json file:
```
{
  "dependencies": {
    "express": "^4.13.3"
  }
}
```
2. Now in GitBash in your project directory, run `npm install`. This will install Express onto your computer.
3. Now that we have our dependencies installed, create a server.js:
```
// This file creates a simple server for us to use
// Not important to understand
var
  express = require('express'),
  app = express();

app.use(express.static(__dirname + '/', {}));

app.get('/', function (req, res) {
  res.sendFile(__dirname + '/index.html');
});

app.listen(9000);
console.log('Magic happens on port 9000');
```
4. This server is used to serve a basic website by sending HTML/JS files to the browser. These files will let the browser send requests to the API we made. Also notice that we used port 9000, which must be different from the first port we used.
5. Now download and drag app.module and app.config (from this Github repo) into the current directory.
6. 
