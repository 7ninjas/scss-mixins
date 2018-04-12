# _shapes.scss
_File includes mixin which helps in creating triangles in css_

### List of content:

- [Mixin triangle](#mixin-triangle)


## Mixin triangle

### Description
_Mixin which helps setting transition properties to given class_

### Parameters
- `$color` - color of shape (***required***)
- `$direction` - shape's corner direction (***required***)
- `$size` - shape's size (**default ```6px```**)
- `$position` - position of shape (**default ```absolute```**)
- `$round` - boolean if corner should be rounded (**default ```false```**)

### Usage: 
Created rounded shape with $color-grey color and up direction

```scss
.exampleTransitionClass {
  @include triangle($color: $color-grey, $direction: up, $round: true);
}
```
