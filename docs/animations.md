# _animations.scss
_File includes mixin for hardware acceleration for some animation_

### List of content:

- [Mixin hardware](#mixin-hardware)

## Mixin hardware

### Description
_Simple and effective for when you need to trigger hardware acceleration for some animation, keeping everything fast, slick and flicker-free._

### Parameters
- `$backface` - set `hidden` value for `backface-visibility` property. (**default `true`**)
- `$perspective` - gives an element a 3D-space by affecting the distance between the Z plane and the user. (**default
 `1000`**)

### Usage: 

Enable hardware acceleration for elements with `exampleAnimationClass` class. 


#### Case 1
Assign hardware acceleration with default values. 

```scss
.exampleAnimationClass {
    @include hardware;
}
```

#### Case 2
Assign hardware acceleration without `backface-visibility` property. 

```scss
.exampleAnimationClass {
    @include hardware(false);
}
```

#### Case 3
Assign hardware acceleration. Set custom value `perspective` property.

```scss
.exampleAnimationClass {
    @include hardware($perspective: 5000);
}
```