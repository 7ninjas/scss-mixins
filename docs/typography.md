# _typography.scss
_File includes mixins which help create consistent and proper styling of fonts_

### List of content:

- [Mixin text-hide](#mixin-text-hide) (bootstrap 4.0.0)
- [Mixin text-truncate](#mixin-text-truncate) (bootstrap 4.0.0)
- [Mixin font](#mixin-font)


### Default variables
_Default variables declared in file will be used mainly in ```font``` mixin._

```scss
$typography: (
  base: (
    base: (
      font-family: 'Proxima Nova' sans-serif,
      font-size: $font-size-base,
      font-weight: 400,
      letter-spacing: 1px,
      line-height: 1.3
    )
  ),
  h1: (
    base: (
      font-size: 26px,
      font-weight: 500,
      letter-spacing: 3px,
      line-height: 1.5
    ),
    sm: (
      font-size: 16px,
      letter-spacing: 2px,
      line-height: 1.8
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
_Mixin for truncating text.   
It requires inline-block or block for proper styling._

### Usage: 
Truncating text in specific class

```scss
.exampleTruncateTextClass {
    @include text-truncate();
}
```


## Mixin font

### Description
_Mixin which helps assign consistent font values for given class_

### Parameters
- `$variant` - font variant which should be assigned to font (```$typography``` will be search through for this 
value) (**default ```base```**)
- `$color` - color which should be assigned to font
- `$line-height` - line height which should be assigned to font
- `$align` - text alignment which should be assigned to font
- `$responsive` - font responsiveness

### Usage: 

#### Case 1
Set `h1` font variation from `$typography` variable map.
In this case h1 contains styles for base and sm variation. 
That means that for sm breakpoint and narrower styles will be applied from sm variation. 
For there rest - styles will be taken from base variation.

```scss
.exampleClass {
   @include font(h1);
}
```

#### Case 2
Set `h1` font variation styles from `$typography` variable and change font color for all breakpoints.

```scss
.exampleClass {
   @include font(h1, $color-black);
}
```

#### Case 3
Set `h1` font variation styles from `$typography` variable and change text align for all breakpoints.

```scss
.exampleClass {
   @include font(h1, $align: right);
}
```

#### Case 5
Set `h1` font variation styles and disable applying styles for breakpoints defined for `h1` variant in `$typography` variable.

```scss
.exampleClass {
   @include font(h1, $responsive: false);
}
```
