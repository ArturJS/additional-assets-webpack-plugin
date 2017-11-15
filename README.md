additional-assets-webpack-plugin
=============================

Generate additional assets during webpack compilation process with ability to hash and minify them.

Install
-------

```
npm install --save-dev additional-assets-webpack-plugin
```

Usage
-----

```javascript
const AdditionalAssetsWebpackPlugin = require('additional-assets-webpack-plugin');

const webpackConfig = {
    plugins: [
        new AdditionalAssetsWebpackPlugin({
              assets: [
                {
                  name: 'prebootInit',
                  filename: 'prebootInit-[hash].js',
                  sourceCode: 'console.log('Hello world!')',
                  uglifyJs: true
                }
              ]
            }),
    ]
    // other webpack config ...
}
```
