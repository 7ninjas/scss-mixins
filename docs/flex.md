# _flex.scss
_File includes mixins which helps use flex features in easiest way_

### List of content:

- [Mixin flex](#mixin-flex)
- [Mixin inline-flex](#mixin-inline-flex)
- [Mixin flex-variant](#mixin-flex-variant)


## Mixin flex

### Description
_Mixin which helps to add `display: flex;` property to the class, 
alternatively set `flex-direction`, `align-items`, `justify-content` and `flex-wrap` properties._

### Parameters
- `$direction` - defines the direction of items in the flex container
- `$cross` - defines how flex items are laid out along the cross axis
- `$main` - defines the alignment along the main axis
- `$wrap` - defines how flex items will wrap onto multiple lines

### Usage: 

#### Case 1
Assign property `display: flex;` to the class without any extra properties.

```
.exampleFlex {
   @include flex();
}
```

#### Case 2
Assign `display: flex` property to the class and define the direction of items in the flex container.

```
.exampleFlex {
    @include flex($direction: column);
}
```

#### Case 3
Assign `display: flex` property to the class and define how flex items are laid out along the cross axis.

```
.exampleFlex {
   @include flex($align-items: flex-end);
}
```

#### Case 4
Assign `display: flex` property to the class and defines alignment of flex items along the main axis.

```
.exampleFlex {
   @include flex($main: space-between);
}
```

#### Case 5
Assign `display: flex` property to the class and wrap flex items onto multiple lines.

```
.exampleFlex {
   @include flex($wrap: wrap);
}
```



## Mixin inline-flex

### Description
_Mixin which helps to add `display: inline-flex;` property to the class, 
alternatively set `flex-direction`, `align-items`, `justify-content` and `flex-wrap` properties._

### Parameters
- `$direction` - defines the direction of items in the flex container
- `$cross` - defines how flex items are laid out along the cross axis
- `$main` - defines the alignment along the main axis
- `$wrap` - defines how flex items will wrap onto multiple lines

### Usage: 

#### Case 1
Assign property `display: inline-flex;` to the class without any extra properties.

```
.exampleFlex {
   @include flex();
}
```

#### Case 2
Assign `display: inline-flex` property to the class and define the direction of items in the flex container.

```
.exampleFlex {
    @include flex($direction: column);
}
```

#### Case 3
Assign `display: inline-flex` property to the class and define how flex items are laid out along the cross axis.

```
.exampleFlex {
   @include flex($align-items: flex-end);
}
```

#### Case 4
Assign `display: inline-flex` property to the class and defines alignment of flex items along the main axis.

```
.exampleFlex {
   @include flex($main: space-between);
}
```

#### Case 5
Assign `display: inline-flex` property to the class and wrap flex items onto multiple lines.

```
.exampleFlex {
   @include flex($wrap: wrap);
}
```


## Mixin flex-variant

### Description
_Helper mixin which helps to create `flex` and `inline-flex` mixins_

### Parameters
- `$display` - defines type of flex element
- `$direction` - defines the direction of items in the flex container
- `$cross` - defines how flex items are laid out along the cross axis
- `$main` - defines the alignment along the main axis
- `$wrap` - defines how flex items will wrap onto multiple lines
