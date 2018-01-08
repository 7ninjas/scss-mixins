# _typography.scss
_File includes mixins which help create consistent and proper styling of fonts_

### List of content:

- [Mixin text-hide](#mixin-text-hide) (bootstrap 4.0.0-beta)
- [Mixin text-truncate](#mixin-text-truncate) (bootstrap 4.0.0-beta)
- [Mixin _font-variant](#mixin-_font-variant)
- [Mixin font](#mixin-font)
- [Mixin link-variant](#mixin-link-variant)


### Default variables
_Default variables declared in file will be used mainly in ```font``` mixin._

```scss
$font-variants: (
  base: (
    base: (
      font-size: $font-size-base,
    )
  ),
  h1: (
    base: (
      font-size: 4rem,
    ),
    sm: (
      font-size: 2rem,
    )
  ),
) !default;
```

## Mixin text-hide

### Description
_Mixin for text hiding_

### Usage: 
Hiding text in given class

```scss
.exampleHideTextClass {
    @include text-hide();
}
```

## Mixin text-truncate

### Description
_Mixin for truncating text.<br />
It requires inline-block or block for proper styling._

### Usage: 
Truncating text in specific class

```scss
.exampleTruncateTextClass {
    @include text-truncate();
}
```

## Mixin _font-variant

### Description
_Helper (mixin) which is used in ```font``` mixin for assigning values to proper keys_

### Parameters
- `$styles` - mapable object with variables like ```font-family```, ```font-size```, ```font-weight```, ```letter-spacing```, ```text-transform``` (**required**)
- `$color` - color which should be assigned to font (as default it's used ```false```)
- `$line-height` - line height which should be assigned to font (as default it's used ```false```)
- `$align` - text alignment which should be assigned to font (as default it's used ```false```)


## Mixin font

### Description
_Mixin which helps assign consistent font values for given class_

### Parameters
- `$variant` - font variant which should be assigned to font (```$font-variants``` will be search through for this value) (as default it's used ```base```)
- `$color` - color which should be assigned to font (as default it's used ```false```)
- `$line-height` - line height which should be assigned to font (as default it's used ```false```)
- `$align` - text alignment which should be assigned to font (as default it's used ```false```)
- `$responsive` - font responsiveness (as default it's used ```true```)

### Usage: 
Assigning h1 font variation with red color and without responsiveness

```scss
.exampleClass {
   @include font($variant: h1, $color: #ff0000, $responsive: false);
}
```

## Mixin link-variant

### Description
_Mixin styling color to given one, setting cursor type to pointer and setting adequate values ​​for hover and focus actions<br />
Mainly used for consistent links styling._

### Parameters
- `$color` - name of color (**required**)

### Usage: 
Styling link with blue color

```scss
.exampleLinkClass {
    @include link-variant(#0000ff);
}
```