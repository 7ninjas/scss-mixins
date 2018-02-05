# _border-radius.scss
_File includes mixins which help to keep consistent border radiuses._

### List of content:

- [Mixin border-radius](./docs/border-radius.md#mixin-border-radius) (bootstrap 4.0.0)
- [Mixin border-top-radius](./docs/border-radius.md#mixin-border-top-radius) (bootstrap 4.0.0)
- [Mixin border-right-radius](./docs/border-radius.md#mixin-border-right-radius) (bootstrap 4.0.0)
- [Mixin border-bottom-radius](./docs/border-radius.md#mixin-border-bottom-radius) (bootstrap 4.0.0)
- [Mixin border-left-radius](./docs/border-radius.md#mixin-border-left-radius) (bootstrap 4.0.0)


### Default variables
_Default variables declared in file to be used in mixins._

```scss
$color-primary: #999;
$enable-rounded: false !default;
$border-radius: 1px solid $color-primary !default;
```

## Mixin border-radius

### Description
_Mixin which uses variable `$enable-rounded`. If it's true borders will be rounded. Otherwise - it won't do anything._

### Parameters
- `$radius` - defines properties of wanted border radius (**default ```$border-radius```**)

### Usage: 
Assign border radius with properties 1px solid and color defined in variables as `$red`

```scss
.exampleBorderClass {
    @include border-radius (1px solid $red);
}
```
