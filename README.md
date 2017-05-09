# Canivete with Webpack

Example of Canivete use with [Webpack](https://webpack.js.org/).

1. In the Terminal, go to your project's root folder.

```shell
$ cd canivete-with-webpack
```

2. Install Canivete via NPM.

```shell
$ npm install --save leofavre/canivete
```

3. Install Webpack via NPM.

```shell
$ npm install --save-dev webpack
```

4. Create a file named "webpack.config.js" in your project's root folder with the following content:

```js
const path = require("path");

module.exports = {
	entry: "./index.js",
	output: {
		path: path.resolve(__dirname, "dist"),
		filename: "app.js"
	}
};
```

5. Create a file named "index.js" in your project's root folder. Import any dependencies from Canivete (or other libraries) using ES6 modules syntax, before the rest of your code, like this:

```js
import toAverage from "canivete/dist/toAverage";

const myArray = [8, 10, 12, 14, 16];
alert(myArray.reduce(toAverage));
// => 12
```

6. Finally, use the following shell command to build your project:

```shell
$ ./node_modules/.bin/webpack
```
