# _grid.scss
_File includes breakpoint viewport sizes and media queries._

### List of content:

- [Mixin center](#mixin-center)
- [Mixin container](#mixin-container)
- [Mixin col](#mixin-col)


### Default variables
_Default variables which are required in mixins located in file. They are set with most common values._

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
Setting child element centered relatively to parent element

```scss
.exampleParentClass {

    .exampleChildClass {
        @include center();
    }
}
```


## Mixin container

### Description
_Mixin which helps with proper displaying container with flex property and 100% width._

### Parameters
- `$fluid` - variable which indicates if container should be fluid (as default it's used ```$grid-fluid```)
- `$gutter` - object with width of gutters for different resolutions  (as default it's used ```$grid-gutter-widths```)
- `$max-widths` - object with max width of container for different resolutions (as default it's used ```$container-max-widths```)

### Usage: 
Assigned fluid grid for container without gutters.

```scss
.exampleContainerClass {
     @include container(true, $gutter: false);
}
```


## Mixin col

### Description
_Mixin which helps with indicate number of columns with their size, gutters, offset and alignment._

### Parameters
- `$size` - variable which indicates size of each column (as default it's used ```$grid-columns```)
- `$columns` - variable which indicates number of columns  (as default it's used ```$grid-columns```)
- `$gutter-widths` - variable which indicates width of each gutter (as default it's used ```$grid-gutter-widths```)
- `$offset` - variable which indicates size of offset (as default it's used ```0```)
- `$align` - variable which indicates alignment of columns (as default it's used ```auto```)

### Usage: 


#### Case
Set 12 columns with size 24 and left alignment to given class

```scss
.exampleColClass {
    @include col($size: 24, $columns: 12, $align: left);
}
```

