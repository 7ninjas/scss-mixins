# _fonts.scss
_File includes helper for adding @font-face rules_

### List of content:

- [Mixin font-face](#mixin-font-face)

## Mixin font-face

### Description
_Specify a font name, URL where it can be found, font weight and font style._

### Parameters
- `$font-name` - defines a name for the font (**required**)
- `$file-name` - name of font files with path (**required**)
- `$weight` - defines the boldness of the font. Default value is "normal".
- `$style` - defines how the font should be styled. Default value is "normal".

### Usage:

#### Case 1

Define font Poppins from `../fonts` folder.

```
@include font-face(Poppins, '../fonts/poppins-v3-latin-ext-500', 500, italic);
```
Each kind of font's file have to have the same naming pattern. For example:
```javascript
poppins-v3-latin-ext-500.eot
poppins-v3-latin-ext-500.woff
poppins-v3-latin-ext-500.ttf
poppins-v3-latin-ext-500.svg
```

#### Case 2 - **Using mixin along with `css-modules`**

**NOTE:**
While using `face-font` mixin along with `css-modules` for best optimization you should place it in component which is used in whole application.
Best place for that is inside scss file for CoreLayout component. Thanks to that it will be imported only once and not in every component.
It's very important to place it outside of any class declaration.

Define font Graphik from `../fonts` folder.
```javascript
@include font-face(Graphik Regular, '../fonts/Graphik-Regular');
@include font-face(Graphik Light, '../fonts/Graphik-Light');
@include font-face(Graphik Medium, '../fonts/Graphik-Medium');
@include font-face(Graphik Semibold, '../fonts/Graphik-Semibold');

.sampleClass {
...
}
```