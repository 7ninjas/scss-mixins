# _colors.scss
_File includes function which helps keeping consistent shades of color_

### List of content:

- [Function color](#function-color)


### Default variables
_Default variables declared in file to be used in ```colors``` map and later in ```color``` function.<br />
In variables map of colors and colors themselves can be redeclared._

```scss
$color-primary: red !default;
$color-secondary: blue !default;
$color-shade-amount: 15% !default;
$color-trans-amount: 0.5 !default;

$colors: (
  primary: (
    base: $color-primary,
    light: lighten($color-primary, $color-shade-amount),
    dark: darken($color-primary, $color-shade-amount),
    trans: transparentize($color-primary, $color-trans-amount)
  ),
  secondary: (
    base: $color-secondary,
    light: lighten($color-secondary, $color-shade-amount),
    dark: darken($color-secondary, $color-shade-amount),
    trans: transparentize($color-secondary, $color-trans-amount)
  )
) !default;
```

## Function color

### Description
_Function which helps to retrieve color from colors map_

### Parameters
- `$color-name` - name of color from map (**required**)
- `$color-variant` - color variant from ```colors``` map (as default it's used ```base```)

### Usage: 
Assigned light shade of primary color to class

```scss
.exampleClass {
    color: color(primary, light)
}
```
