<hr>
## Installation

* git clone https://github.com/apocas/outkept
* npm install
* Ajust conf/*.js files according to your needs. Instructions [here](configuration).
* node main.js

Installation is pretty simple, configuration is a bit more demanding. Follow the instructions and `Outkept` will be your best friend for all those repeating tasks you are always doing when something happens in your cluster.

<hr>
## Dependencies

You only have to attend to the global dependencies, npm awesomeness will take care of the rest.

### Global

* Git (or just curl/wget zip from Github)
* Node
* Redis

### node.js (`npm install` will take care of this for you)

* ssh2 - module used for all SSH communications with all servers.
* emailjs - email module.
* lynx - Statsd module.
* ntwitter - Twitter API implementation.
* express - Web framework.
* hiredis - Redis communication.
* redis - Redis communication.
* feedparser - RSS feed parser.
* request - HTTP request.
* forever-monitor - Process state control.
* optimist - Option parsing.
* reconnect - Reconncetion control between browser and server.
* shoe - WebSocket emulation.
* duplex-emitter - Two way event stream.

[meta:title]: <> (Instructions)
