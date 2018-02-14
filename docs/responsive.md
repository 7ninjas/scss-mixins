# _responsive.scss
_File includes mixins which helps to make responsive grid columns, embed objects and create responsible properties_

### List of content:

- [Mixin responsive-prop](#mixin-responsive-prop)
- [Mixin responsive-embed](#mixin-responsive-embed)
- [Mixin responsive-col](#mixin-responsive-col)


## Mixin responsive-prop

### Description
_Mixin which helps create css properties for each breakpoints_

### Parameters
- `$prop` - css property (***required***)
- `$breakpoints` - object with specified values for each needed screen resolution (***required***)
### Usage: 

Assigned top margin for different screen resolutions

```scss
.exampleClass {
  @include responsive-prop(margin-top, (xxl: 160px, xl: 160px, lg: 130px, md: 100px, sm: 70px, xs: 50px));
  
  @include responsive-prop(margin-top, (
    down xs: 30px,
    sm: 50px,
    between md lg: 80px,
    up xl: 150px
  ));
}
```

## Mixin responsive-embed

### Description
_Mixin which helps make embed objects responsible_

### Parameters
- `$x` - value of horizontal aspect ratio (**default ```16```**)
- `$y` - value of vertical aspect ratio (**default ```9```**)
- `$selector` - value of media selector (**default ```> :first-child```**)

### Usage: 
Assigned media with aspect ratio 4:3

```scss
.exampleResponsiveMediaClass {
  @include responsive-embed(4,3);
}
```


## Mixin responsive-col

### Description
_Mixin which helps handling with size of columns on different screen resolutions_

### Parameters
- `$breakpoints` - object with specified values for each needed screen resolution (***required***)

### Usage: 
Assigned size of columns for different screen resolutions. 

```scss
.exampleCol {
   @include responsive-col((
     down sm: 12,
     between md lg: 3,
     up xl: 2
   ));
}
```
Mixin `responsive-col` helps to create columns for different breakpoints in simpler way  in contrast to the way implemented below

```scss
  .exampleClass {
    @include media-breakpoint-up(xl) {
      @include col(2);
    }
  
    @include media-breakpoint-between(md, lg) {
      @include col(3);
    }
  
    @include media-breakpoint-down(sm) {
      @include col(12);
    }
  }

```
