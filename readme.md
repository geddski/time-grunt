# time-grunt [![Build Status](https://travis-ci.org/sindresorhus/time-grunt.svg?branch=master)](https://travis-ci.org/sindresorhus/time-grunt)

> Display the elapsed execution time of [grunt](http://gruntjs.com) tasks

![screenshot](screenshot.png)


## Usage

```sh
$ npm install --save-dev time-grunt
```

```js
// Gruntfile.js
module.exports = function (grunt) {
	// require it at the top and pass in the grunt instance
	require('time-grunt')(grunt);

	grunt.initConfig();
}
```

## Optional Callback

If you want to collect the timing stats for your own use, pass a callback to time-grunt:

```js
require('time-grunt')(grunt, function (stats, done) {
	// do whatever you want with the stats
	uploadReport(stats);
	
	// be sure to let grunt know when to exit
	done();
});
```

## Clean layout

Tasks that take less than 1% of the total time are hidden to reduce clutter.

Run grunt with `grunt --verbose` to see all tasks.


## License

MIT © [Sindre Sorhus](http://sindresorhus.com)
