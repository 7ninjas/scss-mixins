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
  down sm: 40px,
  up sm: 30px,
) !default;
$container-max-widths: (
  sm: 540px,
  md: 720px,
  lg: 960px,
  xl: 1140px
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
- `$fluid` - variable which indicates if container should be fluid (**default ```$grid-fluid```**)
- `$gutter` - object with width of gutters for different resolutions  (**default ```$grid-gutter-widths```**)
- `$max-widths` - object with max width of container for different resolutions (**default ```$container-max-widths```**)

### Usage:

#### Case 1
Assigned grid container with gutters
```scss
.exampleContainerClass {
     @include container();
}
```

#### Case 2
Assigned fluid grid container.

```scss
.exampleContainerClass {
     @include container(true);
}
```

#### Case 3
Assigned grid container without gutters.

```scss
.exampleContainerClass {
     @include container(true, $gutter: false);
}
```

## Mixin col

### Description
_Mixin which helps to create columns with their size, gutters, offset and alignment._

### Parameters
- `$size` - variable which define size of each column (**default `12`**)
- `$columns` - variable which define number of columns (**default `12`**)
- `$gutter` - variable which define width of each gutter (**default values for each breakpoints defined in ```$grid-gutter-widths```**)
- `$offset` - variable which define size of offset (**default `0`**)
- `$align` - variable which define alignment of columns (**default `auto`**)

### Usage:

#### Case 1
Define styles for block that used 12 column out of the possible default 12 per container.
```scss
.exampleColumn {
    @include col;
}
```


#### Case 2
Define styles for block that used 3 column out of the possible default 12 per container.
```scss
.exampleColumn {
    @include col(3);
}
```

#### Case 3
Define styles for block that used 2 column out of the possible 5 per container.
```scss
.exampleColumn {
    @include col(2, 5);
}
```


#### Case 4
Define styles for block that used 2 column out of the possible 12 and set 5 columns offset.
```scss
.exampleColumn {
    @include col(2, $offset: 5);
}
```

#### Case 5
Define styles for block that used 2 column out of the possible 12 and align it to the center of the container.
```scss
.exampleColumn {
    @include col(2, $align: center);
}
```

#### Case 6
Define styles for block that used 2 column out of the possible 12 and removed gutters.
```scss
.exampleColumn {
    @include col(2, $gutter: false);
}
```
