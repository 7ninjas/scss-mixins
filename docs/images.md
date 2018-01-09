# _images.scss
_File includes bootstrap mixins for images._

### List of content:

- [Mixin img-fluid](#mixin-img-fluid) (bootstrap 4.0.0-beta)
- [Mixin img-retina](#mixin-img-retina) (bootstrap 4.0.0-beta)


## Mixin img-fluid

### Description
_Mixin for keeping image from scaling beyond the width of their parents_

### Parameters
- `$name` - name of breakpoint (included in `$grid-breakpoints`) (**required**)
- `$breakpoints` - map defined in the `$grid-breakpoints`

### Usage: 


#### Case
Changing font size for devices with higher screen resolution than small devices

```scss
.exampleClass {
    @include media-breakpoint-up (sm) {
        font-size: 16px;
    }
}
```


## Mixin img-retina

### Description
_Media of at most the maximum breakpoint width. No query for the largest breakpoint.<br />
Makes the content of class apply to the given breakpoint and narrower._

### Parameters
- `$name` - name of breakpoint (included in `$grid-breakpoints`) (**required**)
- `$breakpoints` - map defined in the `$grid-breakpoints`

### Usage: 


#### Case
Changing font size for devices with lower screen resolution than large devices

```scss
.exampleClass {
    @include media-breakpoint-down (lg) {
        font-size: 14px;
    }
}
```