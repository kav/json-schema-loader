# Json Schema Loader

## Installation

```
npm install json-schema-loader --save
```

## Description

Webpack loader that resolves both internal and external [json schema](json-schema.org) references (`$ref` properties). The loader uses [json-schema-ref-parser](https://github.com/BigstickCarpet/json-schema-ref-parser) to resolve references. Based on [@pr0da/json-schema-loader](https://github.com/pr0da/json-schema-loader).

## Usage

```js
var resolvedSchema = require('json-schema-loader!./schema.json');
```

Or define it in your `webpack.config.js`

```js
module: {
  loaders: [{
    test: /\.json$/,
    exclude: /node_modules/,
    loader: 'json-schema-loader'
  }]
}
```
```js
var resolvedSchema = require('./schema.json');
```
