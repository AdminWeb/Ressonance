Resonance
=========

An agnostic framework PHP library for realtime.

Requirements
------------------
PHP >= 5.5
Redis Server
NodeJS >= 6


Usage
--------
Install dependencies on ```/vendor/bin/package.json```.

Configure port and channels on ```/vendor/bin/config.json```.

Star the server in background with [forever](https://www.npmjs.com/package/forever) or [PM2](https://www.npmjs.com/package/pm2).

Implements the ```Resonance\BeatInterface``` on your classes on your app.

Create a new Bell instance for use touch (method) your beat (implements BeatInterface) (like example folder).

On Front
------------
Put  a tg script with src attribute with value ```http://server-address:server-port/socket.io/socket.io.js```.

Initialize the connection with

```javascript
var conn = io.connect('http://server-address:server-port/your-channel');
conn.on('your-event',function(music){
console.log('your music', music)
});
```
Be happy =D



