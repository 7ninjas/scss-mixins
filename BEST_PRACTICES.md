<p align="center">
  <a href="https://7ninjas.com/">
    <img src="https://7ninjas.com/assets/7ninjas-logo-250x250.gif" alt="" width=72 height=72>
  </a>

  <h3 align="center">7ninjas</h3>

  <p align="center">
    `scss-mixins` is a collection of scss mixins and functions to ease and improve implementations of common style-code patterns.
    <br>
    <br>
    <a href="https://7ninjas.com/case-studies/">Portfolio</a>
    ◦
    <a href="https://7ninjas.com/careers/">Careers</a>
    ◦
    <a href="https://7ninjas.com/contact/">Contact</a>
  </p>
</p>


<h2 align="center">Best Practices - SCSS Styleguide</h2>
This styleguide document is a key document in a project's life and development. It describes how and why code should be 
written that way. When used effectively Sass will help in keeping clean, easily maintainable and DRY codebase. 
However if it's used incorrectly it may add unnecessary or duplicate code. 

Below we present series of hints and tips with which will help 
you get the best out of Sass.

### Table of content

- help yourself with <b>stylelint</b>
- reboot.css or normalize.css
- naming conventions
  - don't reuse parent's class name in child's classes
  - keep order of declaring classes and it states (firstly declare state of current class then declare nested children ie. .active is higher than nested child class)
  - class should be described by entity, behaviour, state or look
  - camelCase in react, rest in hypen-case
  - color naming
- spaces and indentations (2) (no tabs)
- use mixins for margins and paddings
- don't use hardcoded values in scss
- assign value to variable in variables.scss
- first use mixins, then override styles (if needed)
- [Nesting elements](#nesting-elements)
- [Styling classes](#styling-classes)
- [Use class instead of ID](#use-class-instead-of-id)
- don't use id if not needed
- global styles
- styles from another packages
- creating JavaScript-specific classes to bind to, prefixed with .js-


### Nesting elements

We are pretty sure that you've heard or read tale about Little Red Riding Hood. Her mother told her to go straight way 
to Grandma's house and not stray from the path. The girl promised but soon forgot about her mother's warning. That's how she got in troubles.

With nesting elements story is pretty the same. If we nest too much child elements in parent element code will be dirty and messed, so we will have problems while searching for specific class.
We consider maximum 3 levels of nesting as a good practice. To help keep it you should use stylelint for it.

Good practice:
```scss
.container {
  .header {
    .navigation {
      //styles
    }
  }
}
```

Bad practice:
```scss
.container {
  .header {
    .navigation {
      .firstElement {
        .firstElementsChild {
          ...
          //styles
        }
      }
    }
  }
}
```

### Styling classes

You should never style element. It's better to add unique class and style it. While styling elements you override previous style of given element.
It may cause unwanted conflicts while using the same element in another place.

Good practice:
```scss
@import '~@7ninjas/scss-mixins/all';

.title {
  @include font(h1);
}
```

Bad practice:
```scss
@import '~@7ninjas/scss-mixins/all';

h1 {
  @include font(h1);
}
```

### Use class instead of ID

Using ids for styling is considered as one of bad practices. As you should already know classes are reusable and ids are unique. 
Scss doesn't care if you use id or class but efficiency of your further work does.

Good practice:
```scss
@import '~@7ninjas/scss-mixins/all';

.title {
  @include font(h1);
}
```

Bad practice:
```scss
@import '~@7ninjas/scss-mixins/all';

#title {
  @include font(h1);
}
```