# reload-server-webpack-plugin

> Webpack plugin that automatically (re)starts your server between builds.

---

### Why?

- Remove your dependency on `nodemon`, `forever`, `pm2`, or similar.
- This works better from a "cold start" when your server hasn't been built yet.
- Fewer issues with websockets & hot-module reloading.

### Installation

```shell
$ npm install --save-dev reload-server-webpack-plugin
```

### Usage

Update your `webpack.config.js`:

```js
module.exports = {
  ...
  plugins: [
    new ReloadServerPlugin({
      // Defaults to process.cwd() + "/server.js"
      script: "path/to/server.js",
    }),
  ],
  ...
};
```
