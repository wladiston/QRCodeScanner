# Cordova / Ionic Plugin QRCodeScanner

A simple qrcode scanner plugin for **Cordova** / **PhoneGap** / **Ionic** apps. This plugin is a simplification of [phonegap/phonegap-plugin-barcodescanner](https://github.com/phonegap/phonegap-plugin-barcodescanner).

## Installation

    cordova plugin add https://github.com/wladiston/QRCodeScanner
	// or
    ionic plugin add https://github.com/wladiston/QRCodeScanner

### Supported Platforms

- iOS

## Using the plugin ##
The plugin creates the object `cordova.plugin.qrcodeScanner` with the method `scan(success, fail, config)`. 

`success` and `fail` are callback functions. Success is passed an object with data, type and cancelled properties. Data is the text representation of the barcode data, type is the type of barcode detected and cancelled is whether or not the user cancelled the scan.

A full example could be:
```javascript
	var config = {
		cancelButtonTitle: 'Cancelar'
	};

   cordova.plugins.qrcodeScanner.scan(
      function (result) {
          alert('We got a barcode\n' +
                'Result: ' + result.text + '\n' +
                'Cancelled: ' + result.cancelled);
      }, 
      function (error) {
          alert('Scanning failed: ' + error);
      },
      config
   );
```


## Thanks on Github ##

* The [complete plugin](https://github.com/phonegap/phonegap-plugin-barcodescanner).
* The [iOS lib](https://github.com/YannickL/QRCodeReaderViewController).

## Licence ##

The MIT License (MIT)

Copyright (c) 2015 Wladiston Paiva

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
