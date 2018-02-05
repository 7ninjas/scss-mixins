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
$body-bg: $white!default;
```

## Mixin gradient-bg

### Description
_Mixin which helps to create background. Uses global `$enable-gradients` variable to indicate if background should be 
plain color or gradient_

### Parameters
- `$color` - define background color

### Usage: 
Assigned `$color-primary-darker` background color

```scss
.exampleBackgroundGradient {
    @include gradient-bg($color-primary-darker);
}
```


## Mixin gradient-x

### Description
_Mixin which helps to create horizontal gradient, from left to right_

### Parameters
- `$start-color` - define start gradient color (**default `#555`**)
- `$end-color` - define end gradient color (**default `#333`**)
- `$start-percent` - declare where you want to start `$start-color` (**default `0%`**)
- `$end-percent` - declare where you want to stop `$end-color` (**default `100%`**)

### Usage: 
Assigned horizontal background gradient to class

```scss
.exampleGradient {
    @include gradient-x(#000, #fff, 10%, 90%);
}
```


## Mixin gradient-y

### Description
_Mixin which helps to create vertical gradient, from top to bottom_

### Parameters
- `$start-color` - define start gradient color (**default `#555`**)
- `$end-color` - define end gradient color (**default `#333`**)
- `$start-percent` - declare where you want to start `$start-color` (**default `0%`**)
- `$end-percent` - declare where you want to stop `$end-color` (**default `100%`**)

### Usage: 
Assigned vertical background gradient to class

```scss
.exampleGradient {
    @include gradient-y(#f00, #0f0, 10%, 90%);
}
```


## Mixin gradient-directional

### Description
_Mixin which helps to create directional gradient_

### Parameters
- `$start-color` - define start gradient color (**default `#555`**)
- `$end-color` - define end gradient color (**default `#333`**)
- `$deg` - define an angle to specify direction of the gradient (**default `45deg`**)

### Usage: 
Assigned directional background gradient to class

```scss
.exampleGradient {
    @include gradient-directional(30deg, #f00, #0f0);
}
```


## Mixin gradient-x-three-colors

### Description
_Mixin which helps to create horizontal three colors gradient from left to right_

### Parameters
- `$start-color` - define start gradient color (**default `#00b3ee`**)
- `$mid-color` - define middle gradient color (**default `#7a43b6`**)
- `$end-color` - define end gradient color (**default `#c3325f`**)
- `$color-stop` - define position of `$mid-color` from left to right (**default `50%`**)

### Usage: 
Assigned horizontal three-colors background gradient to class

```scss
.exampleThreeColorsGradient {
   @include gradient-x-three-colors(#f00, #0f0, 80%, #00f);
}
```


## Mixin gradient-y-three-colors

### Description
_Mixin which helps to create vertical three colors gradient from top to bottom_

### Parameters
- `$start-color` - define start gradient color (**default `#00b3ee`**)
- `$mid-color` - define middle gradient color (**default `#7a43b6`**)
- `$end-color` - define end gradient color (**default `#c3325f`**)
- `$color-stop` - define position of `$mid-color` from top to bottom (**default `50%`**)

### Usage: 
Assigned vertical three-colors background gradient to class

```scss
.exampleThreeColorsGradient {
   @include gradient-y-three-colors(#f00, #0f0, 40%, #00f);
}
```


## Mixin gradient-radial

### Description
_Mixin which helps to create radial gradient_

### Parameters
- `$inner-color` - define start gradient color (**default `#555`**)
- `$outer-color` - define end gradient color (**default `#333`**)

### Usage: 
Assigned radial gradient with the shape of a circle

```scss
.exampleRadialGradient {
   @include gradient-radial(#f00, #0f0);
}
```


## Mixin gradient-striped

### Description
_Mixin which helps to create striped gradient_

### Parameters
- `$color` - define gradient color (**default `rgba(255,255,255,.15)`**)
- `$angle` - define an angle to specify direction of the gradient (**default `45deg`**)

### Usage: 
Assigned striped gradient to the class

```scss
.exampleStripedGradient {
   @include gradient-striped(#f0f, 30deg);
}
```
