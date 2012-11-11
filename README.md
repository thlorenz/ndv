# DocumentVision

DocumentVision is a [node.js](http://nodejs.org) library for processing and understanding scanned documents.

## Features

- Image manipulation using [Leptonica](http://www.leptonica.com/) (Version 1.69) and [LodePNG](http://lodev.org/lodepng/) (Version 20121027)
- OCR using [Tesseract](http://code.google.com/p/tesseract-ocr/) (Version 3.02)
- Barcode reading using [ZXing](http://code.google.com/p/zxing/) (Version 2.10)

## Installation

	[sudo] npm install [-g] dv

## Quick Start

Once you've installed, download [that image](https://github.com/schulzch/node-dv/blob/master/test/fixtures/textpage300.png). You can use any other image containing simple text at 300dpi or higher. Now run the following code snipped to recognize text from your image:

	var dv = require('dv');
	var fs = require('fs');
	var image = new dv.Image('png', fs.readFileSync('textpage300.png'));
	var tesseract = new dv.Tesseract('.', 'eng', image);
	console.log(tesseract.findText('plain'));

## Whats next?

Here are some quick links to help you get started:

- [API Reference](https://github.com/schulzch/node-dv/wiki/API)
- [Troubleshooting](https://github.com/schulzch/node-dv/wiki/Troubleshooting)
- [Bug Tracker](https://github.com/schulzch/node-dv/issues)

## License

Licensed under the incredibly [permissive](http://en.wikipedia.org/wiki/Permissive_free_software_licence) [MIT License](http://creativecommons.org/licenses/MIT/). Copyright &copy; 2012 Christoph Schulz.
