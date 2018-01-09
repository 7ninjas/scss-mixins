# _hover.scss
_File includes mixins which helps with styling elements with actions (hover, focus, active)._

### List of content:

- [Mixin hover](#mixin-hover) (bootstrap 4.0.0-beta)
- [Mixin hover-focus](#mixin-hover-focus) (bootstrap 4.0.0-beta)
- [Mixin plain-hover-focus](#mixin-plain-hover-focus) (bootstrap 4.0.0-beta)
- [Mixin hover-focus-active](#mixin-hover-focus-active) (bootstrap 4.0.0-beta)


## Mixin hover

### Description
_Mixin for styling element when it's hovered_

### Usage: 
Assigned different color for hovered element

```scss
.exampleHoveredClass {
    color: #222;
    @include hover() {
        color: #555;
    }
}
```


## Mixin hover-focus

### Description
_Mixin for styling element when it's hovered and focused_

### Usage: 
Assigned different color of element when it's hovered and focused

```scss
.exampleHoveredFocusClass {
    color: #222;
    @include hover-focus() {
        color: #555;
    }
}
```


## Mixin plain-hover-focus

### Description
_Mixin for styling element when it's hovered, focused and doesn't have set any action_

### Usage: 
Set color of element when it's plain, hovered and focused

```scss
.examplePlainHoveredFocusClass {
    @include plain-hover-focus() {
        color: #555;
    }
}
```


## Mixin hover-focus-active

### Description
_Mixin for styling element when it's hovered, focused and active_

### Usage: 
Assigned different color of element when it's hovered, focused and active

```scss
.exampleHoveredFocusActiveClass {
    color: #222;
    @include hover-focus-active() {
        color: #555;
    }
}
```
