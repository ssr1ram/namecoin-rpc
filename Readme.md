# namecoin-rpc

namecoin-rpc is a simple wrapper for the namecoind client's JSON-RPC API.

This is a fork of the [node-bitcoin])https://github.com/freewil/node-bitcoin) repo and has been adapted for namecoin

The methods are exposed as lower camelcase methods on the `rpc.Client`
object, or you may call the API directly using the `cmd` method.

## Install

Coming soon... `npm install namecoin-rpc`

## Examples

### Create client
```js
// all config options are optional
var rpc = require('namecoin-rpc');
var client = new rpc.Client({
  host: 'localhost',
  port: 8336,
  user: 'username',
  pass: 'password',
  timeout: 30000
});
```

### GetInfo

```js
client.getInfo( [], function(err, result, resHeaders) {
  if (err) return console.log(err);
  console.log(result);
});
```
### GetIno directly using `cmd`

```js
client.cmd('getinfo', [], function(err, result, resHeaders){
  if (err) return console.log(err);
  console.log(result);
});
```
