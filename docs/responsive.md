# _responsive.scss
_File includes mixins which_

### List of content:

- [Mixin responsive-prop](#mixin-responsive-prop)
- [Mixin responsive-embed](#mixin-responsive-embed)
- [Mixin responsive-breakpoint](#mixin-responsive-breakpoint)
- [Mixin responsive-col](#mixin-responsive-col)


## Mixin responsive-prop

### Description
_Mixin which helps handling css properties on different screen resolutions_

### Parameters
- `$prop` - css property (***required***)
- `$breakpoints` - object with specified values for each needed screen resolution (***required***)
### Usage: 
Assigned top margin for different screen resolutions for example container

```scss
.exampleResponsivePropClass {
  $margin-top: (xxl: 160px, xl: 160px, lg: 130px, md: 100px, sm: 70px, xs: 50px);
  @include responsive-prop(margin-top, $margin-top);
}
```

## Mixin responsive-embed

### Description
_Mixin which helps handling with media on different screen resolutions_

### Parameters
- `$x` - value of horizontal aspect ratio (as default it's used ```16```)
- `$y` - value of vertical aspect ratio (as default it's used ```9```)
- `$selector` - value of media selector (as default it's used ```> :first-child```)

### Usage: 
Assigned media with aspect ratio 4:3

```scss
.exampleResponsiveMediaClass {
  @include responsive-embed(4,3);
}
```

## Mixin responsive-breakpoint

### Description
_Helper for handling with breakpoints on different screen resolutions_

### Parameters
- `$breakpoint-query` - string with given media breakpoint type and optionally breakpoint name (ie. 'only, down, up, between') (***required***)


## Mixin responsive-col

### Description
_Mixin which helps handling with size of columns on different screen resolutions_

### Parameters
- `$breakpoints` - object with specified values for each needed screen resolution (***required***)

### Usage: 
Assigned size of columns for different screen resolutions for example container

```scss
.exampleResponsiveColClass {
  $breakpoints: (xxl: 200px, xl: 180px, lg: 150px, md: 100px, sm: 80px, xs: 50px);
  @include responsive-col($breakpoints);
}
```
