# _units.scss
_File includes function which helps keeping consistent shades of color_

### List of content:

- [Function strip-unit](#function-strip-unit)
- [Function to-rem](#function-to-rem)


### Default variables
_Default variables declared in file will be used in ```to-rem``` function._

```scss
$font-size-base: 16px !default;
```

## Function strip-unit

### Description
_Helper for ```to-rem``` function to get rid of unit_

### Parameters
- `$value` - value which should should be disposed of unit (**required**)

## Function to-rem

### Description
_Function which helps converting given value to value in rem units with taking base font size into account_

### Parameters
- `$value` - value which should be converted into rem (**required**)

### Usage: 
Changing font size from pixels to rem

```scss
.exampleClass {
    font-size: to-rem(15px);
}
```