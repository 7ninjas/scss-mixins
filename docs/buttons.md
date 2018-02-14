# _buttons.scss
_File includes mixins which helps create consistently styled buttons_

### List of content:

- [Mixin button-variant](#mixin-button-variant) (bootstrap 4.0.0)
- [Mixin button-outline-variant](#mixin-button-outline-variant) (bootstrap 4.0.0)
- [Mixin button-size](#mixin-button-size) (bootstrap 4.0.0)


### Default variables
_Default variables which are required in mixins located in file. They are set with most common values._

```scss
$black: #242222 !default;
$white: #fff !default;
$enable-rounded: false !default;
$btn-focus-width: 2px !default;
$enable-shadows: false !default;
$btn-active-box-shadow: inset 0 3px 5px rgba($black, .125) !default;
$btn-box-shadow: inset 0 1px 0 rgba($white, .15), 0 1px 1px rgba($black, .075) !default;
```


## Mixin button-variant

### Description
_Mixin which helps to create button with specified border and background color when it's hovered_

### Parameters
- `$background` - defines button's text and background color (**required**)
- `$border` - defines button's border color (**required**)
- `$hover-background` - defines button's text and background color when hovered (**default `darken($background, 7.5%)`**)
- `$hover-border` - defines button's border color when hovered (**default `darken($border, 10%)`**)
- `$active-background` - defines button's text and background color when active `$end-color` (**default `darken($background, 10%)`**)
- `$active-border` - defines button's border color when active (**default `darken($border, 12.5%)`**)

### Usage: 
Assign primary color (variable) as button's text and background color and primary dark (variable) as border of button 

```scss
.exampleGradient {
    @include button-variant($color-primary, $color-primary-dark);
}
```


## Mixin button-outline-variant

### Description
_Mixin which helps to create button with specified border and background color when it's hovered_

### Parameters
- `$color` - defines button's text and border color (**required**)
- `$color-hover:` - defines button's color when hovered (**default `color-yiq($color)`**)
- `$active-background` - defines button's color when active (**default `$color`**)
- `$active-border` - defines button's border when active (**default `$color`**)

### Usage: 
Assigned button with $color-primary(variable) color and $color-primary-light(variable) color of border and background
 while active.

```scss
.exampleSizedButton {
    @include button-outline-variant($color: $color-primary, $active-background: $color-primary-light, $active-border: $color-primary-light);
}
```


## Mixin button-size

### Description
_Mixin which helps to keep consistent size of button_

### Parameters
- `$padding-y` - defines vertical padding of button (**required**)
- `$padding-x` - defines horizontal padding of button (**required**)
- `$font-size` - defines font size of button (**required**)
- `$line-height` - defines line height of button (**required**)
- `$border-radius` - defines border radius properties of button (**required**)

### Usage: 
Assigned button with 10px of top and bottom padding, 20px of right and left padding, 16px font size, 20px line height
 and 1px solid border with $color-primary(variable) color

```scss
.exampleSizedButton {
    @include button-size(10px, 20px, 16px, 20px, 1px solid $color-primary);
}
```
