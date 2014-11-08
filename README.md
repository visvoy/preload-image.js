日本語→[README.ja.md](README.ja.md)

# preload-image.js

Common image-preloader.

# Usage

See sample JS. -> [sample/sample.js](sample/sample.js)

Paste content of [preload-image.min.js](preload-image.min.js) and:

```js
preloadImages([
	'path/to/image1',
	'path/to/image2',
	'path/to/image3'
])
	.onprogress(function(data) {
		console.log(
			data.path, 'is loaded.',
			'Status: ',
			data.loadeds.length, '/', data.files.length,
			' : ',
			parseInt(100 * data.loadeds.length / data.files.length, 10) + '%'
			);
		document.body.appendChild(data.image);
	})
	.onload(function(data) {
		console.log('Done.');
	})
	.onerror(function(data) {
		console.error('ERROR!', data.event);
	});
```

# About

## Developed by

* TAKANASHI Ginpei
	* [@ginpei\_jp](https://twitter.com/ginpei_jp)
	* [@ginpei\_en](https://twitter.com/ginpei_en)
	* [ginpei.info](http://ginpei.info/)
* [ginpei/preload-image.js](https://github.com/ginpei/preload-image.js)

## License

* MIT License: [http://opensource.org/licenses/MIT](http://opensource.org/licenses/MIT)

## History

* 2014-11-08
	* First release.
