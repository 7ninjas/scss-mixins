# _fonts.scss
_File includes helper for adding @font-face rules_

### List of content:

- [Mixin font-face](#mixin-font-face)

## Mixin font-face

### Description
_Specify a font name, URL where it can be found, font weight and font style_

### Parameters
- `$font-name` - define a name for the font (**required**)
- `$file-name` - name of font files with path (**required**)
- `$weight` - defines the boldness of the font. Default value is "normal".
- `$style` - defines how the font should be styled. Default value is "normal".

### Usage: 

Changing font size for devices with higher screen resolution than small devices

```
@include font-face(Poppins, '../fonts/poppins-v3-latin-ext-500', 500, italic);
```

