# react-simple
Simple Starter React Application


### Install and Run from Checkout:

```
npm install
npm start
```

The following steps are listed to explain to set-up this simple React project from scratch.

### NPM Set-up:

```
npm init
```
This will create a ```package.json``` file. Install the dependencies with:

```
npm install express --save
npm install express-http-proxy --save
npm install body-parser --save
```

Packages will be installed inside ```node_modules```. Ensure all npm packages are installed with:

```
npm install
```

Create a new folder called ```server```. Create a ```server.js``` to host your site. Can also act as an API proxy if needed to avoid CORS issues.

In ```package.json```, add following to scripts.
```
"start": "node server/server.js"
```

Start server with
```
npm start
```

### JSPM Set-up:

Create a directory called ```app```. Within this directory run:

```
jspm init
```
This will create a file called and ```config.js```.

Install your wanted dependencies:

```
jspm install react
jspm install react-dom
```

This will create a directory called ```jspm_packages``` with ```system.js``` inside. Ensure all npm packages are installed with:


```
jspm install
```

Also see link below for getting started with JSPM:
http://jspm.io/docs/getting-started.html



### Building App:

Within the ```app``` directory, create an ```index.html``` and ```app.js```.

```app.js``` should contain your JS code. For example:
```
import React from 'react'
import ReactDOM from 'react-dom'

var ExampleApplication = React.createClass({.....
```

```index.html``` should contain your start-up HTML. For example:
```
<script src="jspm_packages/system.js"></script>
<script src="config.js"></script>
<script>System.import('app.js')</script>
```

```system.js``` and ```config.js``` are needed for all the JSPM dependencies we need. We also import our ```app.js```



