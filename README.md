# `craco-wasm`

A [`craco`](https://github.com/dilanx/craco) plugin to add support for WASM
modules to CRA apps.

## Usage

```bash
yarn add craco-wasm
```

In `craco.config.js`

```javascript
const cracoWasm = require("craco-wasm")

module.exports = {
    plugins: [cracoWasm()]
}
```

## How?

`create-react-app` is based on Webpack 5, which has experimental support for
WASM modules. In order to enable this support this plugin does two things:

1. Enable the `experiments.asyncWebAssembly` webpack config 
2. Add `/\.wasm$/` to the list of files which are not processed by the
   file-loader in the CRA webpack config
