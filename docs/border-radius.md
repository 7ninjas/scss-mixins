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
Assign border radius with `10px` value

```scss
.exampleBorderClass {
    @include border-radius (10px);
}
```

## Mixin border-top-radius

### Description
_Mixin which uses variable `$enable-rounded`. If it's true - top border will be rounded. Otherwise - it won't do 
anything._

### Parameters
- `$radius` - defines properties wanted properties for top border radius (***required***)

### Usage: 
Assign top border radius with `3px` value

```scss
.exampleTopBorderClass {
    @include border-top-radius (3px);
}
```

## Mixin border-right-radius

### Description
_Mixin which uses variable `$enable-rounded`. If it's true - right borders will be rounded. Otherwise - it won't do 
anything._

### Parameters
- `$radius` - defines wanted properties for right border radius

### Usage: 
Assign right border radius with `12px` value

```scss
.exampleRightBorderClass {
    @include border-right-radius (12px);
}
```

## Mixin border-bottom-radius

### Description
_Mixin which uses variable `$enable-rounded`. If it's true - bottom borders will be rounded. Otherwise - it won't do 
anything._

### Parameters
- `$radius` - defines wanted properties for bottom border radius

### Usage: 
Assign bottom border radius with `30px` value
```scss
.exampleBottomBorderClass {
    @include border-bottom-radius (30px);
}
```

## Mixin border-left-radius

### Description
_Mixin which uses variable `$enable-rounded`. If it's true - left borders will be rounded. Otherwise - it won't do 
anything._

### Parameters
- `$radius` - defines wanted properties for left border radius

### Usage: 
Assign left border radius with default value (`5px`)

```scss
.exampleLeftBorderClass {
    @include border-left-radius ();
}
```
