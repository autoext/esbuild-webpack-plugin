# esbuild-webpack-plugin

Use [esbuild](https://github.com/evanw/esbuild) as minifier for webpack.

## Why is this package?

[彻底告别编译 OOM，用 esbuild 做压缩器](https://zhuanlan.zhihu.com/p/139219361)。

## Install

```bash
$ yarn add esbuild-webpack-plugin --dev
```

## Webpack config

```js
const ESBuildPlugin = require('esbuild-webpack-plugin').default;

module.exports = {
  optimization: {
    minimizer: [
      // For plugin options, please refer: https://github.com/evanw/esbuild
      new ESBuildPlugin({...}),
    ],
  },
};
```

## Test

```shell script
# Get prepared
$ yarn && yarn build

# Minify with terser
$ yarn build:example

# Minify with esbuild
$ yarn build:example:esbuild

# Do not minify
$ yarn build:example:nocompress
```

## LICENSE

MIT
