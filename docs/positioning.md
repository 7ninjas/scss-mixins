# _positioning.scss
_File includes function and mixins which help with positioning different type of elements_

### List of content:

- [Mixin size](#function-size) (bootstrap 4.0.0-beta)
- [Mixin clearfix](#mixin-clearfix) (bootstrap 4.0.0-beta)
- [Function z](#function-z)
- [Mixin pseudo](#mixin-pseudo)
- [Mixin position-variant](#mixin-position-variant)
- [Mixin absolute](#mixin-absolute)
- [Mixin fixed](#mixin-fixed)
- [Mixin relative](#mixin-relative)
- [Mixin sticky](#mixin-sticky)


### Default variables
_Default variables declared in file to be used in mixins._

```scss
$z-indexes: (
  'modal',
  'header',
  'body',
  'footer'
) !default;
```

## Mixin size

### Description
_Bootstrap helper which helps setting width and height of element_

### Parameters
- `$width` - variable describing width (***required***)
- `$height` - variable describing height (as default it's used ```$width```)


## Mixin clearfix

### Description
_Bootstrap mixin which helps with wrapping containers_


## Function z

### Description
_Function which sets z-index value appropriate to name's position in ```$z-indexes```.<br />
Thanks to this solution the order has been preserved for every item.<br />
If ```$z-indexes``` doesn't contain given name there will be displayed error with appropriate information_

### Parameters
- `$name` - string with name which should be included in ```$z-indexes``` (***required***)

### Usage: 
Assigned appropriate z-index for header

```scss
.exampleZClass {
    @include z('header');
}
```


## Mixin pseudo

### Description
_Mixin which helps with positioning element with content, display and position properties._

### Parameters
- `$display` - variable which will be used as a value for ```display``` (as default it's used ```block```)
- `$pos` - variable which will be used as a value for ```position``` (as default it's used ```absolute```)
- `$content` - variable which will be used as a value for ```content``` (as default it's used empty string)

### Usage: 
Assigned element with inline display and fixed position

```scss
.examplePseudoClass {
    @include pseudo($display: inline, $pos: fixed);
}
```


## Mixin position-variant

### Description
_Helper for position mixins which helps handling position type and optionally top right bottom and left properties_

### Parameters
- `$position` - variable which will be used as a value for ```position``` (***required***)
- `$args` - variable(s) which will be used as a value(s) for ```top right bottom left``` properties (***required***)


## Mixin absolute

### Description
_Mixin which helps to add position absolute with additional (optional) properties to class_

### Parameters
- `$args` - variable(s) which will be used as a value(s) for ```top right bottom left``` properties (as default it's used empty string)

### Usage: 
Assigned position absolute without additional properties

```scss
.exampleAbsoluteClass {
    @include absolute();
}
```


## Mixin fixed

### Description
_Mixin which helps to add position fixed with additional (optional) properties to class_

### Parameters
- `$args` - variable(s) which will be used as a value(s) for ```top right bottom left``` properties (as default it's used empty string)

### Usage: 
Assigned position fixed without additional properties

```scss
.exampleFixedClass {
    @include fixed();
}
```

## Mixin relative

### Description
_Mixin which helps to add position relative with additional (optional) properties to class_

### Parameters
- `$args` - variable(s) which will be used as a value(s) for ```top right bottom left``` properties (as default it's used empty string)

### Usage: 
Assigned position relative without additional properties

```scss
.exampleRelativeClass {
    @include relative();
}
```

## Mixin sticky

### Description
_Mixin which helps to add position sticky with additional (optional) properties to class_

### Parameters
- `$args` - variable(s) which will be used as a value(s) for ```top right bottom left``` properties (as default it's used empty string)

### Usage: 
Assigned position sticky without additional properties

```scss
.exampleStickyClass {
    @include sticky();
}
```