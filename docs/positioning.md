# _positioning.scss
_File includes _

### List of content:

- [Function z](#function-z)
- [Mixin pseudo](#mixin-pseudo)
- [Mixin position-variant](#mixin-position-variant)
- [Mixin absolute](#mixin-absolute)
- [Mixin fixed](#mixin-fixed)
- [Mixin relative](#mixin-relative)
- [Mixin sticky](#mixin-sticky)


### Default variables
_Default variables declared in file to be used in mixins._

```scss
$z-indexes: (
  'modal',
  'header',
  'body',
  'footer'
) !default;
```

## Function z

### Description
_Helper used in mixins to find proper size with given key_

### Parameters
- `$size` - variable which will be used as a value for ```$spacing-sizes``` map (**required**)


## Mixin ml

### Description
_Mixin which helps to add ```margin-left``` to class_

### Parameters
- `$size` - variable which will be used as a value for ```margin-left``` (as default it's used ```1```)

### Usage: 
Assigned 2rem of left margin to class

```scss
.exampleClass {
    @include ml(4);
}
```


## Mixin mt

### Description
_Mixin which helps to add ```margin-top``` to class_

### Parameters
- `$size` - variable which will be used as a value for ```margin-top``` (as default it's used ```1```)

### Usage: 
Assigned 2rem of top margin to class

```scss
.exampleClass {
    @include mt(4);
}
```


## Mixin mr

### Description
_Mixin which helps to add ```margin-right``` to class_

### Parameters
- `$size` - variable which will be used as a value for ```margin-right``` (as default it's used ```1```)

### Usage: 
Assigned 2rem of right margin to class

```scss
.exampleClass {
    @include mr(4);
}
```


## Mixin mb

### Description
_Mixin which helps to add ```margin-bottom``` to class_

### Parameters
- `$size` - variable which will be used as a value for ```margin-bottom``` (as default it's used ```1```)

### Usage: 
Assigned 2rem of bottom margin to class

```scss
.exampleClass {
    @include mb(4);
}
```


## Mixin mx

### Description
_Mixin which helps to add ```margin-right``` and ```margin-left``` to class_

### Parameters
- `$r` - value for ```margin-right``` (as default it's used ```1```)
- `$l` - value for ```margin-left``` (as default it's used ```null```)

### Usage: 
Assigned 2rem of right margin and 1rem of left margin to class

```scss
.exampleClass {
    @include mx(4, 3);
}
```


## Mixin my

### Description
_Mixin which helps to add ```margin-top``` and ```margin-bottom``` to class_

### Parameters
- `$t` - value for ```margin-top``` (as default it's used ```1```)
- `$b` - value for ```margin-bottom``` (as default it's used ```null```)

### Usage: 
Assigned 2rem of top margin and 1rem of bottom margin to class

```scss
.exampleClass {
    @include my(4, 3);
}
```
