# _transitions.scss
_File includes mixin which set transition properties_

### List of content:

- [Mixin transitionStyles](#mixin-transitionStyles)


### Default variables
_Default variables declared in file will be used in ```transitionStyles``` mixin._

```scss
$transition-duration: .3s !default;
$transition-timing-function: linear !default;
$transition-delay: 0s !default;
```

## Mixin transitionStyles

### Description
_Mixin which helps setting transition properties to given class_

### Parameters
- `$args` - value of transition property (as default it's used ```all```)
- `$duration` - value of transition duration
- `$function` - value of transition timing function
- `$delay` - value of transition delay

### Usage: 
Assigned transition duration on 0.5s and transition-timing-function on ease-in-out for all transitions

```scss
.exampleTransitionClass {
  @include transitionStyles($duration: 0.5s, $function: ease-in-out);
}
```
