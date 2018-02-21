---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

search: true
---

# web3

## web3_clientVersion

```js
curl -X POST --data '{"jsonrpc":"2.0","method":"web3_clientVersion","params":[],"id":67}'
```

> Result

```json
{
  "id":67,
  "jsonrpc":"2.0",
  "result": "Mist/v0.9.3/darwin/go1.4.1"
}
```

Returns the current client version.

##### Parameters
none

##### Returns

`String` - The current client version

# net

## net_version

```js

curl -X POST --data '{"jsonrpc":"2.0","method":"net_version","params":[],"id":67}'
```

> Result

```json
{
  "id":67,
  "jsonrpc": "2.0",
  "result": "59"
}
```

Returns the current network protocol version.

##### Parameters
none

##### Returns

`String` - The current network protocol version

# eth

## eth_getBalance

Returns the balance of the account of given address.

##### Parameters

1. `DATA`, 20 Bytes - address to check for balance.
2. `QUANTITY|TAG` - integer block number, or the string `"latest"`, `"earliest"` or `"pending"`, see the [default block parameter](#the-default-block-parameter)

```js
params: [
   '0x407d73d8a49eeb85d32cf465507dd71d507100c1',
   'latest'
]
```

##### Returns

`QUANTITY` - integer of the current balance in wei.

```js
curl -X POST --data '{"jsonrpc":"2.0","method":"eth_getBalance","params":["0x407d73d8a49eeb85d32cf465507dd71d507100c1", "latest"],"id":1}'
```

> Result

```json
{
  "id":1,
  "jsonrpc": "2.0",
  "result": "0x0234c8a3397aab58" // 158972490234375000
}
```

