# _breakpoints.scss
_Breakpoint viewport sizes and media queries._

### List of content:

- [Function first](#Function-first)
- [Function last](#Function-last)
- [Function str-split](#Function-str-split)


## Mixin media-breakpoint-up

### Description
_Media of at least the minimum breakpoint width. No query for the smallest breakpoint.<br />
Makes the content of class apply to the given breakpoint and wider._

### Parameters
- `$name` - name of breakpoint (included in `$grid-breakpoints`) (**required**)
- `$breakpoints` - map defined in the `$grid-breakpoints`

### Usage: 


#### Case
Changing font size for devices with higher screen resolution than small devices

```
.exampleClass {
    @include media-breakpoint-up (sm) {
        font-size: 16px;
    }
}
```


## Mixin media-breakpoint-down

### Description
_Media of at most the maximum breakpoint width. No query for the largest breakpoint.<br />
Makes the content of class apply to the given breakpoint and narrower._

### Parameters
- `$name` - name of breakpoint (included in `$grid-breakpoints`) (**required**)
- `$breakpoints` - map defined in the `$grid-breakpoints`

### Usage: 


#### Case
Changing font size for devices with lower screen resolution than large devices

```
.exampleClass {
    @include media-breakpoint-down (lg) {
        font-size: 14px;
    }
}
```


## Mixin media-breakpoint-between

### Description


### Parameters
- `$lower` - name of lower breakpoint (included in `$grid-breakpoints`) (**required**)
- `$upper` - name of upper breakpoint (included in `$grid-breakpoints`) (**required**)
- `$breakpoints` - map defined in the `$grid-breakpoints`

### Usage: 


#### Case
Changing font size for devices with screen resolution between medium and large devices

```
.exampleClass {
    @include media-breakpoint-between (md, lg) {
        font-size: 14px;
    }
}
```


## Mixin media-breakpoint-only

### Description
_Media between the breakpoint's minimum and maximum widths.<br />
No minimum for the smallest breakpoint, and no maximum for the largest one.<br />
Makes the content of class apply only to the given breakpoint, not viewports any wider or narrower._

### Parameters
- `$name` - name of lower breakpoint (included in `$grid-breakpoints`) (**required**)
- `$breakpoints` - map defined in the `$grid-breakpoints`

### Usage: 


#### Case
Changing font size for devices with lower screen resolution than large devices

```
.exampleClass {
    @include media-breakpoint-only (lg) {
        font-size: 14px;
    }
}
```
