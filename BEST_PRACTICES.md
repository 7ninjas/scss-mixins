<p align="center">
  <a href="https://7ninjas.com/">
    <img src="https://7ninjas.com/assets/7ninjas-logo-250x250.gif" alt="" width=72 height=72>
  </a>

  <h3 align="center">7ninjas</h3>

  <p align="center">
    <a href="https://7ninjas.com/case-studies/">Portfolio</a>
    ◦
    <a href="https://7ninjas.com/careers/">Careers</a>
    ◦
    <a href="https://7ninjas.com/contact/">Contact</a>
  </p>
</p>


<h2 align="center">Best Practices - SCSS Styleguide</h2>

<p align="center">You know how it is when project is developed by many programmers. Each of them has his own convention in styling so we have to clean it and order it. 
This document is a key document of styling in a project's life and development created after many hours of practices and researches. We've tried many different
options but finally decided to use on specyfic solution for each problem. This styleguide describes how and why we write code this way. 
Used effectively Sass will help in keeping clean, easily maintainable and DRY codebase. However if it's used incorrectly it may add unnecessary or duplicated code.</p> 

<p align="center">Below we present series of hints and tips with which will help you get the best out of Sass.</p>

<p align="center"><strong>Be like a Ninja! Style like a Ninja!</strong></p>

<br />

### Table of content

- help yourself with <b>stylelint</b>
- creating JavaScript-specific classes to bind to, prefixed with .js-
- reboot.css or normalize.css
- [Naming conventions](#naming-conventions)
- keep order of declaring classes and it states (firstly declare state of current class then declare nested children ie. .active is higher than nested child class)
- spaces and indentations (2) (no tabs)
- use mixins for margins and paddings
- [Margins and paddings](#margins-and-paddings)
- [Values in variables](#values-in-variables)
- [Mixins before styles](#mixins-before-styles)
- [Nesting elements](#nesting-elements)
- [Styling classes](#styling-classes)
- [Use class instead of ID](#use-class-instead-of-id)
- global styles
- styles from another packages


### Naming conventions 

There are several different conventions of naming your classes. Mainly we use hypen-case naming style but in React we always prefer camelCase way.

- Try to avoid reusing parent's name in child's classes. Even if at the first moment it seems pretty logic later it will only cause you headaches. Browser will still read it but you it will be more problematic for you. 
Firstly code isn't as clean as it could be. Secondly because in the end scss will be complied to clearer css form reusing parent's name is unnecessary. 

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
  .containers-header {
    .containers-header-navigation {
      //styles
    }
  }
  .containers-form {
    .containers-form-input{
      //styles
    }
  }
}
```

- We always use specified naming convention for color variables. Firstly we indicate that it's a color, then it goes name of color. In the end we add type of color (if needed).

Good practice:
```scss
$color-primary-darker: #2d2d2d;
$color-primary-dark: #7c7575;
$color-primary: #999;
$color-primary-light: #e6e6e6;
$color-primary-lighter: #fafafa;
```

Bad practice:
```scss
$dark-color: #2d2d2d;
$more-grey-grey: #7c7575;
$grey: #999;
$almost-white: #e6e6e6;
$whiter-than-almost-white: #fafafa;
```

- Remember that it usually makes more sense to name classes based on their meaning, rather than their appearance. Best way 
to name class is to describe it by entity, behaviour or state. Rarely element's change their purpose  - more often they change their attributes.

Good practice:
```scss
.errorMessage {
  color: $color-error;
}
```

Bad practice:
```scss
.redText {
  color: red;
}
```

### Margins and paddings

Using mixins for margins and paddings which we prepared will help you work faster and make your code cleaner if you ever want to maintain it.

Good practice:
```scss
.container {
  @include pl(2);
  @include m(1);
}
```

Bad practice:
```scss
.container {
  padding-left: 20px;
  margin: 10px;
}

### Values in variables

It's always a good practice to store constant values in one file with adequate naming and reuse them properly. 
We believe in clean and ordered codebase so we use file created specially for this purpose - [_variables.scss](./_variables.scss.example) ([Documentation](./docs/variables.md)).
We keep there all important and reusable values. Thanks to that we can easily control number of 
colors we use in project. What's more our graphic designers can standarize them if there are to many various but similar colors.

Good practice:
```scss
.errorMessage {
  color: $color-error;
  
}
```

Bad practice:
```scss
.errorMessage {
  color: red;
}
```

### Mixins before styles

We've seen many different conventions in 

Good practice:
```scss
.container {
  @include p(2, 2, 2, 2);
  @include font(h1, $align: right);
  padding-left: 5px;
}
```

Bad practice:
```scss
.container {
  padding-left: 5px;
  @include p(2, 2, 2, 2);
  @include font(h1, $align: right);

}
```

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
.title {
  @include font(h1);
}
```

Bad practice:
```scss
h1 {
  @include font(h1);
}
```

### Use class instead of ID

Using ids for styling is considered as one of bad practices. As you should already know classes are reusable and ids are unique. 
Scss doesn't care if you use id or class but efficiency of your further work does.

Good practice:
```scss
.title {
  @include font(h1);
}
```

Bad practice:
```scss
#title {
  @include font(h1);
}
```
