
# SpriteSmith TexturePacker (JSON Array) [![NPM Version][npm-image]][npm-url] [![NPM Downloads][npm-download-image]][npm-url]

TexturePacker export template for SpriteSmith - using the array format preferred by Phaser.io

## About

This very tiny module makes exporting TexturePacker compatible JSON sprite sheets
with [grunt-spritesmith](https://github.com/Ensighten/grunt-spritesmith) or
[gulp.spritesmith](https://github.com/twolfson/gulp.spritesmith). Just pass
it along via the `cssTemplate` parameter.

## Example

Building a TexturePacker sprite sheet with [gulp](http://gulpjs.com).

```js

var spritesmith = require('gulp.spritesmith');

gulp.task('sprite', function () {
	return gulp.src('src/gfx/scubaman/*.png')
		.pipe(spritesmith({
			imgName: "scubaman.png",
			cssName: "scubaman.json",
			algorithm: 'binary-tree',
			cssTemplate: require('spritesmith-texturepacker-array') // <-- this right here
		})
		.pipe(gulp.dest('./dist/gfx/'));
});
```

## Install

With npm:

```
npm install spritesmith-texturepacker-array
```

## License
Original Copyright (c) 2014 Mark Riedesel
Licensed under the MIT license.

[npm-url]: https://www.npmjs.org/package/spritesmith-texturepacker-array
[npm-image]: http://img.shields.io/npm/v/spritesmith-texturepacker-array.svg?style=flat
[npm-download-image]: http://img.shields.io/npm/dm/spritesmith-texturepacker-array.svg?style=flat
