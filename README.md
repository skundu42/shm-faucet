### eth-faucet

configure:
create a `config.js` with private key and rpc endpoint.
first namespace is used in `docker-compose.yml`.
```
cp config.js.example config.js
```

Or pass the environment variable `FAUCET_CONFIG_LOCATION` to the build step.

### if you need more eth, dont build a spam bot

contact me or the Ethereum Foundation

### development:

Running `yarn setup` will install and prepare dependencies.

Running `yarn build` will prepare the webapp.

Running `yarn start` starts the server.

Will not work without a `config.js` file. You can run it on a local testnet like `ganache-cli` by pasting one of your generated private keys into a file like this:

```javascript
module.exports = {
  'ropsten': {
    'privateKey': 'Insert Faucet Private Key',
    'rpcOrigin': 'Insert RPC URL'
  }
}
```

### note:
the faucet regularly restarts to ensure its in a good state

### deploy:
continuous deployment is setup via github actions and kubernetes
