# _shapes.scss
_File includes mixin which helps in creating triangles in css_

### List of content:

- [Mixin css-triangle](#mixin-css-triangle)


## Mixin css-triangle

### Description
_Mixin which helps setting transition properties to given class_

### Parameters
- `$color` - color of shape (***required***)
- `$direction` - shape's corner direction (***required***)
- `$size` - shape's size (**default ```6px```**)
- `$position` - position of shape (**default ```absolute```**)
- `$round` - boolean if corner should be rounded (**default ```false```**)

### Usage: 
Created rounded shape with green color and up direction

```scss
.exampleTransitionClass {
  @include css-triangle($color: #00ff00, $direction: up, $round: true);
}
```
