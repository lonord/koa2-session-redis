# koa2-session-redis
A simple redis store of [koa-session](https://github.com/koajs/session)

## Installation

```shell
$ npm install koa2-session-redis
```

## Example

Simple example.

```js
const session = require('koa-session');
const RedisStore = require('koa2-session-redis');
const Koa = require('koa');
const app = new Koa();
//...
const CONFIG = {
  /* other options */
  store: new RedisStore()
};
app.use(session(CONFIG, app));
//...
```

## API

**RedisStore#constructor(config)**

`config` The config argument passed to `createClient(config)` of [node_redis](https://github.com/NodeRedis/node_redis)

## License

MIT