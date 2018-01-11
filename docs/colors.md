# _colors.scss
_File includes function which helps keeping consistent shades of color_

### List of content:

- [Function color](#function-color)


### Default variables
_Default variables declared in file will be used in ```colors``` map and later in ```color``` function.<br />
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
  ),
  gray: (
    base: #999,
    dark: #7c7575,
    darker: #2d2d2d,
    darkest: #242222,
    light: #e6e6e6,
    lighter: #fafafa,
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

#### Case 1
Assigned `base` variant of `gray` color (`#999`) to class

```scss
.exampleClass {
    color: color(gray);
}
```

#### Case 1
Assigned `darkest` variant of `gray` color (`#242222`) to class

```scss
.exampleClass {
    color: color(gray, darkest);
}
```
