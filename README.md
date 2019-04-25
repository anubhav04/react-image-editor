# react-cropper-image-editor

[Cropperjs](https://github.com/fengyuanchen/cropperjs) as React components




## Docs

* [Image Cropper](https://github.com/fengyuanchen/cropper)

## Installation

Install via [npm](https://www.npmjs.com/package/react-cropper-image-editor)

```shell
npm install --save react-cropper-image-editor
yarn add react-cropper-image-editor
```

You need `cropper.css` in your project which is from [cropperjs](https://www.npmjs.com/package/cropperjs).
Since this project have dependency on [cropperjs](https://www.npmjs.com/package/cropperjs), it located in `/node_modules/react-cropper-image-editor/node_modules/cropperjs/dist/cropper.css` or `node_modules/cropperjs/dist/cropper.css` for npm version `3.0.0` later

# Changelog


## Todo
* Unit test

## Quick Example
```js
import React, {Component} from 'react';
import ImageEditorRc from 'react-cropper-image-editor';
import 'cropperjs/dist/cropper.css'; // see installation section above for versions of NPM older than 3.0.0
// If you choose not to use import, you need to assign Cropper to default
// var Cropper = require('react-cropper-image-editor').default

class Demo extends Component {

  render() {
    return (
      <ImageEditorRc
        ref='cropper'
        crossOrigin='true' // boolean, set it to true if your image is cors protected or it is hosted on cloud like aws s3 image server
        src={image source}
        style={{height: 400, width: 400}}
        aspectRatio={16 / 9}
        className={'your custom class'}
        guides={true}
				rotatable={true}
        aspectRatio={16 / 9}
        imageName='image name with extension to download'
        saveImage={functionToSaveImage} // it has to catch the returned data and do it whatever you want
        responseType='blob/base64'
        guides={false}/>
    );
  }
}
```

## Options

### src
* Type: `string`
* Default: `null`

```js
  <ImageEditorRc src='http://fengyuanchen.github.io/cropper/img/picture.jpg' />
```
### alt
* Type: `string`
* Default: `picture`

### crossOrigin
* Type: `string`
* Default: `null`

### aspectRatio
https://github.com/fengyuanchen/cropperjs#aspectratio

### dragMode
https://github.com/fengyuanchen/cropperjs#dragmode

### data
https://github.com/fengyuanchen/cropperjs#setdatadata

### scaleX
https://github.com/fengyuanchen/cropperjs#scalexscalex

### scaleY
https://github.com/fengyuanchen/cropperjs#scalexscaley

### enable
https://github.com/fengyuanchen/cropperjs#enable

### disable
https://github.com/fengyuanchen/cropperjs#disable

### cropBoxData
https://github.com/fengyuanchen/cropperjs#setcropboxdatadata

### canvasData
https://github.com/fengyuanchen/cropperjs#setcanvasdata

### zoomTo
https://github.com/fengyuanchen/cropperjs#zoomto

### moveTo
https://github.com/fengyuanchen/cropperjs#moveto

### rotateTo
https://github.com/fengyuanchen/cropperjs#rotateto

### Other options
Accept all options in the [docs](https://github.com/fengyuanchen/cropperjs#options) as properties.
Except previous mentioned options, other options don't take effect after component mount.

```js
<ImageEditorRc
  src='http://fengyuanchen.github.io/cropper/img/picture.jpg'
  aspectRatio={16 / 9}
  guides={false}
  />
```


## Build

```
npm run build
npm run build-example
```

## Author
Anubhav Chaturvedi(anubhav.techanthusiast@gmail.com)

## License
MIT
