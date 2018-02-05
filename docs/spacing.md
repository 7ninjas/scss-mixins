# _spacing.scss
_File includes function and mixins which add margins and paddings in many variations_

### List of content:

- [Mixin ml](#mixin-ml)
- [Mixin mt](#mixin-mt)
- [Mixin mr](#mixin-mr)
- [Mixin mb](#mixin-mb)
- [Mixin mx](#mixin-mx)
- [Mixin my](#mixin-my)
- [Mixin m](#mixin-m)
- [Mixin pl](#mixin-pl)
- [Mixin pt](#mixin-pt)
- [Mixin pr](#mixin-pr)
- [Mixin pb](#mixin-pb)
- [Mixin px](#mixin-px)
- [Mixin py](#mixin-py)
- [Mixin p](#mixin-p)


### Default variables
_Default variables declared in file to be used in mixins._

```scss
$spacing-sizes: (
  0: 0rem,
  1: 0.25rem,
  2: 0.5rem,
  3: 1rem,
  4: 2rem,
  5: 4rem,
  6: 8rem,
) !default;
$spacing-important: false !default;
```


## Mixin ml

### Description
_Mixin which helps to add ```margin-left``` to class_

### Parameters
- `$size` - variable which will be used as a value for ```margin-left``` (**default ```1```**)

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
- `$size` - variable which will be used as a value for ```margin-top``` (**default ```1```**)

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
- `$size` - variable which will be used as a value for ```margin-right``` (**default ```1```**)

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
- `$size` - variable which will be used as a value for ```margin-bottom``` (**default ```1```**)

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
- `$r` - value for ```margin-right``` (**default ```1```**)
- `$l` - value for ```margin-left``` (**default ```null```**)

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
- `$t` - value for ```margin-top``` (**default ```1```**)
- `$b` - value for ```margin-bottom``` (**default ```null```**)

### Usage: 
Assigned 2rem of top margin and 1rem of bottom margin to class

```scss
.exampleClass {
    @include my(4, 3);
}
```


## Mixin m

### Description
_Mixin which helps to add all margins to class_

### Parameters
- `$t` - value for ```margin-top``` (**default ```1```**)
- `$r` - value for ```margin-right``` (**default ```null```**)
- `$b` - value for ```margin-bottom``` (**default ```null```**)
- `$l` - value for ```margin-left``` (**default ```null```**)

### Usage: 
Assigned 0.25rem of top and bottom margin and 1rem of left margin to class.<br />
Right margin wasn't assigned!

```scss
.exampleClass {
    @include m($t : 1, $b: 1, $l: 3);
}
```

## Mixin pl

### Description
_Mixin which helps to add ```padding-left``` to class.<br />
Adequate to [Mixin ml](#mixin-ml)_


## Mixin pt

### Description
_Mixin which helps to add ```padding-top``` to class.<br />
Adequate to [Mixin mt](#mixin-mt)_


## Mixin pr

### Description
_Mixin which helps to add ```padding-right``` to class.<br />
Adequate to [Mixin mr](#mixin-mr)_


## Mixin pb

### Description
_Mixin which helps to add ```padding-bottom``` to class.<br />
Adequate to [Mixin mb](#mixin-mb)_


## Mixin px

### Description
_Mixin which helps to add ```padding-right``` and ```padding-left``` to class.<br />
Adequate to [Mixin mx](#mixin-mx)_


## Mixin py

### Description
_Mixin which helps to add ```padding-top``` and ```padding-bottom``` to class.<br />
Adequate to [Mixin my](#mixin-my)_


## Mixin p

### Description
_Mixin which helps to add all paddings to class.<br />
Adequate to [Mixin m](#mixin-m)_