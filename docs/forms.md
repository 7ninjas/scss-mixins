# _forms.scss
_File includes mixin which help with styling form elements_

### List of content:
- [Mixin placeholder](#mixin-placeholder)


## Mixin placeholder

### Description
_Mixin which helps with styling placeholder in inputs_

### Usage: 
Changed placeholder's font style on base one and it's color on `$color-primary-light`

```scss
@include placeholder {
  @include font(base, $color-primary-light);
}
```