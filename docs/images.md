# _images.scss
_File includes bootstrap mixins for images._

### List of content:

- [Mixin img-fluid](#mixin-img-fluid) (bootstrap 4.0.0-beta)
- [Mixin img-retina](#mixin-img-retina) (bootstrap 4.0.0-beta)


## Mixin img-fluid

### Description
_Mixin for keeping image from scaling beyond the width of their parents._

### Usage: 
Set maximum relative to the parent and override the height to auto

```scss
.exampleImgFluidClass {
    @include img-fluid;
}
```


## Mixin img-retina

### Description
_Helper for setting background-image and -size in retina._

### Parameters
- `$file-1x` - image's placement for default resolution (**required**)
- `$file-2x` - image's placement for at least 2dppx resolution (**required**)
- `$width-1x` - width of image (**required**)
- `$height-1x` - height of image (**required**)
