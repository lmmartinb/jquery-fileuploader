# jquery-fileuploader
jQuery FileUploader Plugin.

* npmjs: https://www.npmjs.com/package/jquery-fileuploader
* bower: bower info jquery-fileuploader

## Usage
You only need to add the following line to initialize the plugin.

$(div).fileUploader();

### Enabled Options
#### Opt: DefaultImage
Loads a default image into canvas.

```
$('#canvas2').fileUploader({
    defaultImage: 'https://www.codeproject.com/KB/GDI-plus/ImageProcessing2/flip.jpg'
});
```
#### Opt: readonly
Enables readonly canvas.

```
$('#canvas3').fileUploader({
    defaultImage: 'https://www.codeproject.com/KB/GDI-plus/ImageProcessing2/flip.jpg',
    readonly: 1
});
```
#### Opt: fileType
'accept' parameter for file type. The default value is IMAGE.

```
$('#canvas4').fileUploader({
    fileType: FileUploader.Types.VIDEO
});
```
Available Values:
* FileUploader.Types.IMAGE: "image/*"
* FileUploader.Types.VIDEO: "video/*"

#### Opt: extraTrigger
Selector for extraTrigger.

```
<button id="clickExample">Click</button>
...
$('#canvas5').fileUploader({
    extraTrigger: '#clickExample'
});
```

#### Opt: autoplay
Autoplay Option for videos.
Only for FileType = Video.

```
$('#canvas6').fileUploader({
    autoplay: true
});
```

#### Opt: nocontrols
Nocontrols Option for videos.
This option activates option autoplay.

```
$('#canvas6').fileUploader({
    nocontrols: true
});
```

### FileUploader Changes Detection.
When an image is uploaded, it activates an attribute (data-changes) in the container div.

```
$('#canvas2').data('changed');
```
### Video Support.
To use video support, you just need to add fileType option as VIDEO.

## How It Works
This is a simple plugin:

1. Creates a div where the image will be previewed.
2. Initialize fileUploader plugin: $(div).fileUploader();
3. A canvas fill 100% div's area.
4. A hidden input type file will be added.
5. Append onclick event listener in canvas.
6. Onchange event for input file that draw an image into canvas.
7. Rotate canvas reading EXIF data.


## License
```
MIT License

Copyright (c) 2017 - LCApps

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

```

## To-Do List
* FileUploader Options.
    * ~~defaultImage.~~
    * ~~fileType.~~
    * ~~readonly.~~
    * ~~autoplay (only for videos).~~
    * ~~nocontrols (only for videos).~~
    * ~~extraTrigger.~~
* Modal handler.
* Multi image.
* ~~Video support.~~
* Cropper.
* Rotate buttons.
* ~~Any method to detect if an image has changed.~~
* ~~Triggers a fileUploaderChange event. ~~

(If you have any suggestion please feel free to contact me)

## History of Changes
### v1.1.3
loadFrom
fill
fileUploaderChange trigger.

### v1.1.2
ExtraTrigger option.
Autoplay option.
Nocontrols option.

### v1.1.1
Video Support

### v1.1.0
Code refactor.
Fix #1 - Scope Problems.
FileType Option Included.

### v1.0.3
readonly option and data-change attribute added.

### v1.0.2
defaultImage option implemented.

### v1.0.1
Include bower.json

### v1.0.0
Initial version
