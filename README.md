# Eon.js
A simple framework for creating web services

## Why Eon?
Yes, another web server framework. Whenever a new one comes out, you have to ask yourself: Do I need this? Am I fine to just continue using express/fastify/etc...? I want to persent to you the reasons why I began writing this framework and hopefully make your decision a bit easier.

### Express is _not_ a small framework
Express is great, because it provides lots of features, but that also makes it a quite large library. With Eon, I tried to reduce the bundle size by writing as much code as possible on my own and adding only the neccessary features.

### 0 Dependencies
As of `v1.11.5`, Eon.js has *no dependencies whatsoever*, thereby further reducing the bundle size and overhead of additional packages to manage.

# Installation
To install eon, simply run
```bash
npm i eonjs --save
```

# Examples & Usage
Here is an example of using Eon:
```js
// Require Eon
const eon = require('eonjs');
// Create App
// Shorthand: const app = require('eon')(8080);
const app = eon(8080);
// Create a get path
app.get('/').json((req, res) => ({hello: 'world', how_are: 'you?'}));
```