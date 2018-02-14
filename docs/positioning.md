# _positioning.scss
_File includes function and mixins which help with positioning different type of elements_

### List of content:
- [Mixin size](#mixin-size) (bootstrap 4.0.0)
- [Mixin clearfix](#mixin-clearfix) (bootstrap 4.0.0)
- [Mixin z-index](#mixin-z-index)
- [Mixin pseudo](#mixin-pseudo)
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
- `$height` - variable describing height (**default ```$width```**)


## Mixin clearfix

### Description
_Bootstrap helper. Applicable to parent class if children elements use float property. If you don't use this, the container won't get any height_


## Mixin z-index

### Description
_Mixin which sets z-index value appropriate to name's position in ```$z-indexes```.   
Thanks to this solution the order has been preserved for every item.    
If ```$z-indexes``` doesn't contain given name there will be displayed error with appropriate information_

### Parameters
- `$name` - string with name which should be included in ```$z-indexes``` (***required***)

### Usage: 
Assigned appropriate z-index for header

```scss
.exampleZClass {
    @include z-index('header');
}
```


## Mixin pseudo

### Description
_Mixin which helps with positioning pseudo elements with content, display and position properties._

### Parameters
- `$display` - variable which will be used as a value for ```display``` (**default ```block```**)
- `$content` - variable which will be used as a value for ```content``` (**default empty string**)

### Usage: 
Assigned element with inline display and default content

```scss
.examplePseudoClass {
   &:before {
       @include pseudo(block);
       ...
    }
   &:after {
       @include pseudo;
       ...
   }
}
```


## Mixin absolute

### Description
_Mixin which helps to add position absolute with additional (optional) properties to class_

### Parameters
- `$args` - variable(s) which will be used as a value(s) for ```top right bottom left``` properties (**default empty 
string**)

### Usage: 
Assigned position absolute without additional properties

```scss
.exampleAbsoluteClass {
   @include absolute(top 0 left 0 bottom 0);
}
```


## Mixin fixed

### Description
_Mixin which helps to add position fixed with additional (optional) properties to class_

### Parameters
- `$args` - variable(s) which will be used as a value(s) for ```top right bottom left``` properties (**default empty 
string**)

### Usage: 
Assigned position fixed without additional properties

```scss
.exampleFixedClass {
    @include fixed(left 50% bottom 150px);
}
```

## Mixin relative

### Description
_Mixin which helps to add position relative with additional (optional) properties to class_

### Parameters
- `$args` - variable(s) which will be used as a value(s) for ```top right bottom left``` properties (**default empty 
string**)

### Usage: 
Assigned position relative without additional properties

```scss
.exampleRelativeClass {
    @include relative;
}
```

## Mixin sticky

### Description
_Mixin which helps to add position sticky with additional (optional) properties to class_

### Parameters
- `$args` - variable(s) which will be used as a value(s) for ```top right bottom left``` properties (**default empty 
string**)

### Usage: 
Assigned position sticky without additional properties

```scss
.exampleStickyClass {
    @include sticky;
}
```