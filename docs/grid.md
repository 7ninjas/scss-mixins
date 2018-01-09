# _grid.scss
_File includes breakpoint viewport sizes and media queries._

### List of content:

- [Mixin center](#mixin-center)
- [Mixin container](#mixin-container)
- [Mixin col](#mixin-col)


### Default variables
_Default variables which are required in mixins located in file_

```scss
$grid-columns: 12 !default;
$grid-fluid: false !default;
$grid-gutter-widths: (
  xl: 30px,
  lg: 30px,
  md: 30px,
  sm: 30px,
) !default;
$container-max-widths: (
  sm: 576px,
  md: 720px,
  lg: 940px,
  xl: 1140px,
) !default;
```


## Mixin center

### Description
_Mixin for setting auto left and right margins_

### Usage: 
Changing font size for devices with higher screen resolution than small devices

```scss
.exampleClass {
    @include center();
}
```


## Mixin container

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


## Mixin col

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

