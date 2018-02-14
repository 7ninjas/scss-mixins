# _icons.scss
_File includes mixin for styling svg icon._

### List of content:

- [Mixin svg-icon](#mixin-svg-icon)


## Mixin svg-icon

### Description
_Mixin which helps changing size, color and stroke of svg icon_

### Parameters
- `$color` - color which icon should be filled (**default ```false```**)
- `$width` - width of icon (**default ```false```**)
- `$height` - height of icon (**default ```$width```**)

### Usage: 


#### Example
```scss
// Set icons properties so it will be filled with $color-red color, has green stroke and will be 10px width and 20px height.
.exampleClass {
    @include svg-icon($color-red);
}

// Set icons properties so it will be filled with $color-red color and icon size. Height and width of the icon will be 10px
.exampleClass {
    @include svg-icon($color-red, 10px);
}

// Set icons properties so it will be filled with $color-red color and icon size. Height of the icon will be 10px and width 20px
.exampleClass {
    @include svg-icon($color-red, 10px, 20px);
}
```
