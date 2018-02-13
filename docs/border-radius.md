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
$border-radius: 5px !default;
$enable-rounded: true !default;
```

## Mixin border-radius

### Description
_Mixin which uses variable `$enable-rounded`. If it's true - borders will be rounded. Otherwise - it won't do anything._

### Parameters
- `$radius` - defines properties of wanted border radius (**default ```$border-radius```**)

### Usage: 
Assign border radius with properties 1px solid and color defined in variables as `$red`

```scss
.exampleBorderClass {
    @include border-radius (1px solid $red);
}
```

## Mixin border-top-radius

### Description
_Mixin which uses variable `$enable-rounded`. If it's true - top border will be rounded. Otherwise - it won't do 
anything._

### Parameters
- `$radius` - defines properties wanted properties for top border radius (***required***)

### Usage: 
Assign top border radius with properties 1px solid and color defined in variables as `color-primary-light`

```scss
.exampleTopBorderClass {
    @include border-top-radius (1px solid $color-primary-light);
}
```

## Mixin border-right-radius

### Description
_Mixin which uses variable `$enable-rounded`. If it's true - right borders will be rounded. Otherwise - it won't do 
anything._

### Parameters
- `$radius` - defines wanted properties for right border radius

### Usage: 
Assign right border radius with properties 1px solid and color defined in variables as `$color-primary`

```scss
.exampleRightBorderClass {
    @include border-right-radius (1px solid $color-primary);
}
```

## Mixin border-bottom-radius

### Description
_Mixin which uses variable `$enable-rounded`. If it's true - bottom borders will be rounded. Otherwise - it won't do 
anything._

### Parameters
- `$radius` - defines wanted properties for bottom border radius

### Usage: 
Assign bottom border radius with properties 1px solid and color defined in variables as `$color-secondary`

```scss
.exampleBottomBorderClass {
    @include border-bottom-radius (1px solid $color-secondary);
}
```

## Mixin border-left-radius

### Description
_Mixin which uses variable `$enable-rounded`. If it's true - left borders will be rounded. Otherwise - it won't do 
anything._

### Parameters
- `$radius` - defines wanted properties for left border radius

### Usage: 
Assign left border radius with properties 1px solid and color defined in variables as `$color-success`

```scss
.exampleLeftBorderClass {
    @include border-left-radius (1px solid $color-success);
}
```
