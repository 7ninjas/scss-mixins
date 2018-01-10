# _tables.scss
_File includes mixins which helps tables styling_

### List of content:

- [Mixin table](#mixin-table)
- [Mixin table-bordered](#mixin-table-bordered)
- [Mixin table-responsible](#mixin-table-responsible)
- [Mixin table-striped](#mixin-table-striped)
- [Mixin table-hover](#mixin-table-hover)


### Default variables
_Default variables which are required in mixins located in file. They are set with most common values._

```scss
// Table variants
$table-bordered: true !default;
$table-responsible: true !default;
$table-striped: true !default;
$table-hovered: true !default;
    
// Table
$table-background: transparent !default;
$table-cell-padding: 5px !default;
    
// Table striped
$table-strip-color: #000 !default;
$table-strip-opacity: 0.05 !default;
    
// Table hovered
$table-hover-color: #000 !default;
$table-hover-opacity: 0.1 !default;
    
// Table bordered
$table-border-width: 1px !default;
$table-border-color: #e6e6e6 !default;
```

## Mixin table

### Description
_Mixin for styling `table` tag_

### Parameters
- `$bordered` - include mixin `table-bordered`. (**default `true`**)
- `$responsible` - include mixin `table-responsible`. (**default `true`**)
- `$striped` - include mixin `table-striped`. (**default `true`**)
- `$hovered` - include mixin `table-hovered`. (**default `true`**)

### Usage:

#### Case 1
Use mixin without any parameters if you want to make your table bordered, responsible, striped and hovered.

```scss
table.exampleTable {
  @include table();
}
```

#### Case 2
Use mixin with parameter `$bordered: false` if you don't want to make your table bordered.

```scss
table.unborderedTable {
  @include table($bordered: false);
}
```

#### Case 3
Use mixin with parameter `$responsible: false` if you don't want to make your table responsible on mobile devices.

```scss
table.unresponsibleTable {
  @include table($responsible: false);
}
```


#### Case 4
Use mixin with parameter `$striped: false` if you don't want to make your table striped.

```scss
table.unstripedTable {
  @include table($striped: false);
}
```

#### Case 5
Use mixin with parameter `$hovered: false` if you don't want to make your table hovered.

```scss
table.unhoveredTable {
  @include table($hovered: false);
}
```


## Mixin table-bordered

### Description
_Mixin for making tables bordered_

### Parameters
- `$border-width` - (**default `1px`**)
- `$border-color` - (**default `#e6e6e6`**)

### Usage:

#### Case 1
Use mixin with any parameters if you want to use mixin with default variables.

```scss
table.borderedTable {
  @include table-bordered();
}
```

#### Case 2
Use mixin with with parameters if you want to change border width and border color.

```scss
table.borderedTable {
  @include table-bordered(3px, #000000);
}
```


## Mixin table-responsible

### Description
_Mixin for making tables responsible on mobile devices._

### Usage:
Make table horizontal scrollable on devices with small screen resolution.

```scss
table.responsibleTable {
  @include table-bordered();
}
```



## Mixin table-striped

### Description
_Mixin for making tables striped_

### Parameters
- `$color` - (**default `#000`**)
- `$opacity` - (**default `0.05`**)

### Usage:

#### Case 1
Use mixin with any parameters if you want to use mixin with default variables.

```scss
table.stripedTable {
  @include table-striped();
}
```

#### Case 2
Use mixin with with parameters if you want to change color and opacity.

```scss
table.borderedTable {
  @include table-bordered(#f4f500, 0.1);
}
```


## Mixin table-hovered

### Description
_Mixin for making table's rows hoverable_

### Parameters
- `$color` - (**default `#000`**)
- `$opacity` - (**default `0.1`**)

### Usage:

#### Case 1
Use mixin with any parameters if you want to use mixin with default variables.

```scss
table.stripedTable {
  @include table-striped();
}
```

#### Case 2
Use mixin with with parameters if you want to change color and opacity.

```scss
table.borderedTable {
  @include table-bordered(#f4f500, 0.15);
}
```