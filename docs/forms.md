# _forms.scss
_File includes mixins which help to keeping consistent input's and textarea's styles_

### List of content:

- [Mixin resizable](#mixin-flex)
- [Mixin input](#mixin-input)
- [Mixin textarea](#mixin-textarea)


## Mixin resizable

### Description
_Mixin which helps to make element resizable_

### Parameters
- `$direction` - defines the adjusting direction of the block 

### Usage: 

Make block with class `exampleResize` resizable

```scss
.exampleResize {
   @include resizable;
}
```

## Mixin input

### Description
_Mixin which helps to style inputs in form_

### Usage: 
Change input style's properties like `background-color`, `border`, `color`, `padding` and many others. 
User can simply change styles of inputs by changing input variables in `variables.scss`.

```scss
.exampleInput {
   @include input;
}
```


## Mixin textarea

### Description
_Mixin which helps to style textareas in form_

### Usage: 
Change textarea style's properties like `background-color`, `border`, `color`, `padding` and many others. 
Textarea mixin use input mixin to define styles, also it helps to make textarea resizable.
User can simply change styles of textarea by changing input variables in `variables.scss`.

```scss
.exampleTextarea {
   @include textarea;
}
```