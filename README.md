# <img src="https://raw.githubusercontent.com/sadra/EasyMTProto/master/public/images/emtproto.png" width="100px" height="auto"> EasyMTProto

[![Version](https://img.shields.io/badge/version-1.0.0-red.svg?style=flat)](https://github.com/amlashi-sadra/awesome-medium-editor)
[![License](https://img.shields.io/badge/licence-Apache%202.0-lightgrey.svg?style=flat)](https://github.com/amlashi-sadra/awesome-medium-editor)
[![npm version][npm-image]][npm-url]
[![Gitter](https://img.shields.io/badge/gitter-join%20chat-brightgreen.svg?style=flat)](https://gitter.im/Easy-MTProto/Lobby)



Easy Nodejs server app for **Telegram Mobile Protocol** [(MTProto)](https://core.telegram.org/mtproto) in pure **javascript** on the Node.js platform


**Telegram Mobile Protocol** [(MTProto)](https://core.telegram.org/mtproto) unofficial library in pure **javascript** on the Node.js platform

## About MTProto..

**MTProto** is the [Telegram Messenger](http://www.telegram.org ) protocol
_"designed for access to a server API from applications running on mobile devices"_.

The Mobile Protocol is subdivided into three components ([from the official site](https://core.telegram.org/mtproto#general-description)):

 - High-level component (API query language): defines the method whereby API
 queries and responses are converted to binary messages.

 - Cryptographic (authorization) layer: defines the method by which messages
 are encrypted prior to being transmitted through the transport protocol.

 - Transport component: defines the method for the client and the server to transmit
 messages over some other existing network protocol (such as, http, https, tcp, udp).


## Easy-MTProto in short..

The **Easy-MTProto** use [JSMTProxy](https://github.com/FreedomPrevails/JSMTProxy) as the kernel.

## Installation

Get the `easy-mtproto` and install all dependencies:

```bash
$ git clone --branch=master https://github.com/sadra/EasyMTProto
$ cd EasyMTProto
$ npm install
```

Modify the `config.json` parameters to what ever thing you want:

```json
{
  "port": 5665,
  "secret":"b0cbcef5a486d9636472ac27f8e11a9d",
  "server": "10.10.10.10",
  "indexPort": 8080
}
```


| Params        | Propose                       |
| :------------ | :---------------------------- |
| **port**      | The port of MT Protocol       |
| **secret**    | Secret code for MT Protocol. It must be 32 characters and contains numbers & just `a,b,c,d,e,f` for symbols)   |
| **server**    | Your server IP                |
| **indexPort** | Port for index page of app    |
| **channel**   | Your sponsored channel ID (for public channels    |

## Run

### With nodemon

First of all install `nodemon` on you global path: [**nodemo**](https://nodemon.io/)
and then run it with nodmeon
```bash
$ nodemon emtproto.js
```

### With pm2

First of all install `pm2` tool: [**pm2**](http://pm2.keymetrics.io/)
and then run it with nodmeon
```bash
$ pm2 start emtproto.js -i max
$ pm2 list
```


## Use

Before start anything the client mus be updated: [telegram download](https://telegram.org/)

You can share the proxy within a link.

**structure:**

<pre>
https://t.me/proxy?server=<b>SERVER_ADDRESS</b>&port=<b>PORT</b>&secret=<b>SECRET_KEY</b>&@<b>YOUR_CHANNEL_ADDRESS</b>`
</pre>

**example:**

<pre>
https://t.me/proxy?server=10.10.10.10&port=5665&secret=b0cbcef5a486d9636472ac27f8e11a9d&@EasyMTProxy
</pre>

You can get the link from index of your app on your server:
<pre>
SERVER_ADDRESS:INDEX_PORT
//example
http://10.10.10.10:8080
</pre>


## License

The project is released under the [Apache License 2.0](./LICENSE)

[npm-url]: https://www.npmjs.org/package/telegram-mt-node
[npm-image]: https://badge.fury.io/js/telegram-mt-node.svg

[travis-url]: https://travis-ci.org/enricostara/telegram-mt-node
[travis-image]: https://travis-ci.org/enricostara/telegram-mt-node.svg?branch=master

[coverage-url]: https://coveralls.io/r/enricostara/telegram-mt-node?branch=master
[coverage-image]: https://img.shields.io/coveralls/enricostara/telegram-mt-node.svg

[climate-url]: https://codeclimate.com/github/enricostara/telegram-mt-node
[climate-image]: https://codeclimate.com/github/enricostara/telegram-mt-node/badges/gpa.svg

[sauce-url]: https://saucelabs.com/u/telegram-mt-node
[sauce-image]: https://saucelabs.com/browser-matrix/telegram-mt-node.svg