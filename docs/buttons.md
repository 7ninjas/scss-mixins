# _buttons.scss
_File includes mixins which helps create consistently styled buttons_

### List of content:

- [Mixin button-variant](#mixin-button-variant)(bootstrap 4.0.0)
- [Mixin button-outline-variant](#mixin-button-outline-variant)(bootstrap 4.0.0)
- [Mixin button-size](#mixin-button-size)(bootstrap 4.0.0)


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
_Mixin which helps to create horizontal gradient, from left to right_

### Parameters
- `$start-color` - define start gradient color (**default `#555`**)
- `$end-color` - define end gradient color (**default `#333`**)
- `$start-percent` - declare where you want to start `$start-color` (**default `0%`**)
- `$end-percent` - declare where you want to stop `$end-color` (**default `100%`**)

### Usage: 
Assigned horizontal background gradient to class

```scss
.exampleGradient {
    @include gradient-x(#000, #fff, 10%, 90%);
}
```


## Mixin button-outline-variant

### Description
_Mixin which helps to create button with specified border and background color when it's hovered_

### Parameters
- `$color` - define button's color (**default `#555`**)
- `$color-hover:` - define button's color when hovered (**default `color-yiq($color)`**)
- `$active-background` - define button's color when active (**default `$color`**)
- `$active-border` - define button's border when active (**default `$color`**)

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
- `$padding-y` - define vertical padding of button
- `$padding-x` - define horizontal padding of button
- `$font-size` - define font size of button
- `$line-height` - define line height of button
- `$border-radius` - define border radius properties of button

### Usage: 
Assigned button with 10px of top and bottom padding, 20px of right and left padding, 16px font size, 20px line height
 and 1px solid border with $color-primary(variable) color

```scss
.exampleSizedButton {
    @include button-size(10px, 20px, 16px, 20px, 1px solid $color-primary);
}
```
