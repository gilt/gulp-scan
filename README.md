# gulp-scan [![Build Status](https://travis-ci.org/shellscape/gulp-scan.svg?branch=master)](https://travis-ci.org/shellscape/gulp-scan)

A plugin to scan a file for a string or expression


## &nbsp;
<p align="center">
  <b>:rocket: &nbsp; Are you ready to tackle ES6 and hone your JavaScript Skills?</b> &nbsp; :rocket:<br/>
  Check out these outstanding <a href="https://es6.io/">ES6 courses</a> by <a href="https://github.com/wesbos">@wesbos</a>
</p>
---

## Install

```
$ npm install --save-dev gulp-scan
```


## Usage

```js
var gulp = require('gulp');
var scan = require('gulp-scan');

gulp.task('default', function () {
	return gulp.src('src/file.ext')
		.pipe(scan({ term: '@import', fn: function (match, file) {
			// do something with {String} `match`
			// `file` is a clone of the vinyl file.
		}}));
});
```


## API

### scan(options)

#### options

##### term

Type: `string` or `RegExp`  

A term to scan the file for. Can be either a string or regular expression.

##### fn

Type: `Function`  

A function that will receive the individual matches found in a file.

## License

MIT © [Gilt Groupe](https://github.com/gilt)
