# _gradients.scss
_File includes mixins which helps create color gradients_

### List of content:

- [Mixin gradient-bg](#mixin-gradient-bg) (bootstrap 4.0.0)
- [Mixin gradient-x](#mixin-gradient-x) (bootstrap 4.0.0)
- [Mixin gradient-y](#mixin-gradient-y) (bootstrap 4.0.0)
- [Mixin gradient-directional](#mixin-gradient-directional) (bootstrap 4.0.0)
- [Mixin gradient-x-three-colors](#mixin-gradient-x-three-colors) (bootstrap 4.0.0)
- [Mixin gradient-y-three-colors](#mixin-gradient-y-three-colors) (bootstrap 4.0.0)
- [Mixin gradient-radial](#mixin-gradient-radial) (bootstrap 4.0.0)
- [Mixin gradient-striped](#mixin-gradient-striped) (bootstrap 4.0.0)


### Default variables
_Default variables which are required in mixins located in file. They are set with most common values._

```scss
$white: #fff !default;
$enable-gradients: false !default;
$body-bg: $white !default;
```

## Mixin gradient-bg

### Description
_Mixin which helps to set background color. Uses global `$enable-gradients` variable to indicate if background should
 be plain color or gradient. If variable is set `true` background is set to `linear gradient` with `180deg` repeated 
horizontally._

### Parameters
- `$color` - defines background color

### Usage: 
Assigned `$color-primary-darker` as background color

```scss
.exampleBackgroundGradient {
    @include gradient-bg($color-primary-darker);
}
```


## Mixin gradient-x

### Description
_Mixin which helps to create horizontal gradient, from left to right_

### Parameters
- `$start-color` - defines start gradient color (**default `#555`**)
- `$end-color` - defines end gradient color (**default `#333`**)
- `$start-percent` - defines where you want to start `$start-color` (**default `0%`**)
- `$end-percent` - defines where you want to stop `$end-color` (**default `100%`**)

### Usage: 
Assigned horizontal background gradient to class with `$color-white` and `$color-black` color properties which starts
 in 10% and finishes in 90% of area

```scss
.exampleGradient {
    @include gradient-x($color-black, $color-white, 10%, 90%);
}
```


## Mixin gradient-y

### Description
_Mixin which helps to create vertical gradient, from top to bottom_

### Parameters
- `$start-color` - defines start gradient color (**default `#555`**)
- `$end-color` - defines end gradient color (**default `#333`**)
- `$start-percent` - defines  where you want to start `$start-color` (**default `0%`**)
- `$end-percent` - defines  where you want to stop `$end-color` (**default `100%`**)

### Usage: 
Assigned vertical background gradient to class with `$color-white` and `$color-yellow` color properties

```scss
.exampleGradient {
    @include gradient-y($color-red, $color-yellow);
}
```


## Mixin gradient-directional

### Description
_Mixin which helps to create directional gradient_

### Parameters
- `$start-color` - defines start gradient color (**default `#555`**)
- `$end-color` - defines end gradient color (**default `#333`**)
- `$deg` - defines an angle to specify direction of the gradient (**default `45deg`**)

### Usage: 
Assigned directional background gradient to class with `$color-yellow` and `$color-orange` color properties

```scss
.exampleGradient {
    @include gradient-directional(30deg, $color-yellow, $color-orange);
}
```


## Mixin gradient-x-three-colors

### Description
_Mixin which helps to create horizontal three colors gradient from left to right_

### Parameters
- `$start-color` - defines start gradient color (**default `#00b3ee`**)
- `$mid-color` - defines middle gradient color (**default `#7a43b6`**)
- `$color-stop` - defines position of `$mid-color` from left to right (**default `50%`**)
- `$end-color` - defines end gradient color (**default `#c3325f`**)

### Usage: 
Assigned horizontal three-colors background gradient to class with `$color-white`, `$color-grey` and `$color-black` 
color properties

```scss
.exampleThreeColorsGradient {
   @include gradient-x-three-colors($color-white, $color-grey, 80%, $color-black);
}
```


## Mixin gradient-y-three-colors

### Description
_Mixin which helps to create vertical three colors gradient from top to bottom_

### Parameters
- `$start-color` - defines start gradient color (**default `#00b3ee`**)
- `$mid-color` - defines middle gradient color (**default `#7a43b6`**)
- `$color-stop` - defines position of `$mid-color` from top to bottom (**default `50%`**)
- `$end-color` - defines end gradient color (**default `#c3325f`**)

### Usage: 
Assigned vertical three-colors background gradient to class with `$color-white`, `$color-grey` and `$color-black` 
color properties

```scss
.exampleThreeColorsGradient {
   @include gradient-y-three-colors($color-white, $color-grey, 40%, $color-black);
}
```


## Mixin gradient-radial

### Description
_Mixin which helps to create radial gradient_

### Parameters
- `$inner-color` - defines start gradient color (**default `#555`**)
- `$outer-color` - defines end gradient color (**default `#333`**)

### Usage: 
Assigned radial gradient with the shape of a circle to class with `$color-pink` and `$color-purple` color properties

```scss
.exampleRadialGradient {
   @include gradient-radial($color-pink, $color-purple);
}
```


## Mixin gradient-striped

### Description
_Mixin which helps to create striped gradient_

### Parameters
- `$color` - defines gradient color (**default `rgba(255,255,255,.15)`**)
- `$angle` - defines an angle to specify direction of the gradient (**default `45deg`**)

### Usage: 
Assigned striped gradient to class with `$color-orange` color property

```scss
.exampleStripedGradient {
   @include gradient-striped($color-orange, 30deg);
}
```
