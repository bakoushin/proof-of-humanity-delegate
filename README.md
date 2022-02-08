# Proof-of-Humanity Delegate

This repository provides an example of Proof-of-Humanity with a delegate using [hCaptcha](https://www.hcaptcha.com/) verification model.

More details including video are provided in the main contract repo: https://github.com/bakoushin/proof-of-humanity#readme

## Demo

Live demo: https://proof-of-humanity-delegate.glitch.me/

The demo works on the **Rinkeby** testnet. Get test Ether for Rinkeby testnet: https://faucets.chain.link/rinkeby 

## UI

`Delegate` implements basic UI for submitting proof-of-humanity using [hCaptcha](https://www.hcaptcha.com/).

The UI is deliberately made using plain HTML, CSS and vanilla JavaScript in order to not affect the example with any framework specifics. 

## API

Method for generating evidence based on [hCaptcha](https://www.hcaptcha.com/) `token` and `address` ownership `signature`:

### Request

```
POST /api/v1/evidence/
Content-Type: application/json

{
  address: <hex string>
  R: <hex string>
  signature: <hex string>
  token: <hex string>
}
```

### Response

```
{
  timestamp: <hex string>,
  evidence: <hex string>
}
```

## Other parts of the project

* Core contract: https://github.com/bakoushin/proof-of-humanity
* Core UI: https://github.com/bakoushin/proof-of-humanity-core-ui

## Author

Alex Bakoushin

## License

MIT
