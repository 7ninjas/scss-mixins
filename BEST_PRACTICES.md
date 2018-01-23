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
Used effectively Sass will help in keeping clean, easily maintainable and DRY code base. However if it's used incorrectly it may add unnecessary or duplicated code.</p> 

<p align="center">Below we present series of hints and tips with which will help you get the best out of Sass.</p>

<p align="center"><strong>Be like a Ninja! Style like a Ninja!</strong></p>

<br />

### Table of content

- [Stylelint](#stylelint)
- [Clear default styles](#clear-default-styles)
- [Naming conventions](#naming-conventions)
- [Declaring order](#declaring-order)
- [Consistent spacing](#consistent-spacing)
- [Margins and paddings](#margins-and-paddings)
- [Values in variables](#values-in-variables)
- [Mixins before styles](#mixins-before-styles)
- [Nesting elements](#nesting-elements)
- [Styling classes](#styling-classes)
- [Use class instead of ID](#use-class-instead-of-id)
- [Unremovable empty classes](#unremovable-empty-classes)
- [Styles from another packages](#styles-from-another-packages)
- [Global styles](#global-styles)

### Stylelint

We totally recommend you using stylelint while creating stylesheets in your project. It will help avoiding errors and 
enforce you to use consistent conventions. Linter will analyze your piece of code and if it doesn't pass the rules defined in 
linter's configuration it will report errors in console so you know what rule has been broken.

Official website: [Stylelint](https://stylelint.io/)

### Clear default styles

While starting new project it is good to clear default browser styles. That's way we recommend you importing reboot
.css file from [Bootstrap](https://getbootstrap.com/) or normalize.css from [Normalize](https://necolas.github
.io/normalize.css/).

Good practice:
```scss
:global {
  @import '~bootstrap/scss/reboot';
}
```

### Naming conventions 

There are several different conventions of naming your classes. Mainly we use hypen-case naming style but in React we always prefer camelCase way.

- Try to avoid reusing parent's name in child's classes. Even if at the first moment it seems pretty logic later it will only cause you headaches. Browser will still read it but you it will be more problematic for you. 
Firstly code isn't as clean as it could be. Secondly because in the end scss will be complied to clearer css form reusing parent's name is unnecessary. 

Good practice:
```scss
.container {
  .header {
    .navigation {
      ...
    }
  }
}
```

Bad practice:
```scss
.container {
  .containers-header {
    .containers-header-navigation {
      ...
    }
  }
  .containers-form {
    .containers-form-input{
      ...
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

### Declaring order 

As you already should know we like to keep our code base clear and transparent. That's the main reason why we keep order while declaring classes and their states. 

We follow the rule that first state of current class should be declared, then we declare nested children. Thanks to 
that we can easily see what properties given class can accept before focusing on child classes. Doing it in reverse 
order can mislead you while reading code.

Good practice:
```scss
.container {
  .active {
    ...
  }
  .hovered {
    ...
  }
  
  .button {
    .hovered {
      ...
    }
    .text {
      ...
    }
  }
}
```

Bad practice:
```scss
.container {
  .button {
    .text {
      ...
    }
    .hovered {
      ...
    }
        
    }
  .active {
    ...
  }
  .hovered {
    ...
  }
}
```

### Consistent spacing

It's very important to keep consistent spacing in whole project. It makes it more easy to read for any developer who will ever have to work with you code.

In our opinion you should always use spaces instead of tabs. Why? Because tab may be represented by a different number of 
columns depending on your environment and a space is always one column. We also recommend to keep it in 2 indentations. To help with keeping it clean you should use stylelint.

Good practice:
```scss
.container {
  @include pl(2);
  @include m(1);
  
  .title {
    ...
  }
}
```

Bad practice:
```scss
.container {
     @include pl(2);
      @include m(1);
      
          
          
        .title {
         ...
        }}
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
```

### Values in variables

It's always a good practice to store constant values in one file with adequate naming and reuse them properly. 
We believe in clean and ordered code base so we use file created specially for this purpose - [_variables.scss](./_variables.scss.example) ([Documentation](./docs/variables.md)).
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

In styling there are two opposite theories about using mixin in specified order within class. First one says
that firstly you should use mixin and then declare you own styles. Second one claims that you should do it in opposite order.

We practice the first one and we believe that you should too. It will make your work more clear and lucid. Thanks to that solution
you can easily override mixins styles and while maintaining it will help you understand styles order faster. 

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
We consider maximum 3 levels of nesting as a good practice. To help with keeping it clean you should use stylelint.

Good practice:
```scss
.container {
  .header {
    .navigation {
      ...
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

### Unremovable empty classes

<b>This rule we use only in no React projects.</b> 

Sometimes in projects you need to get an element by it's class name using JavaScript. To make it easier to find, know
 it's destination or just tell future developer to not remove it we use specific convention while naming it. To class's 
 name we add `js-` prefix. Also what is important - this class should remain empty to be sure it is used only to find
 specific element by this class.

Good practice:
```scss
.js-specific-class {}
```

Bad practice:
```scss
.specific-class {
  @include font(h1);
  color: $red-error;
}
```

### Styles from another packages

While importing styles from another packages you should always use tilde before package's name instead of full path 
from node modules. It will make your stylesheet easier to read and faster you will know which package you are using.

Good practice:
```scss
.container {
  @import '~bootstrap/scss/reboot';
}  
```

Bad practice:
```scss
.container {
  @import 'node_modules/bootstrap/scss/reboot';
}  
```

### Global styles

Sometimes we find a package with pretty awesome feature we want to add in our project but it doesn't fit our design. 
To solve this problem good practice is to overwrite feature's styles with our own but in React it may be very tricky 
(especially while using CSS Modules). That's why we recommend overwriting them in `:global` class. 

Thanks to that during build step given class will be clear without any dynamically generated, unique, and mapped to the 
correct styles additional text. They won't be scoped to particular templates but will be accessible from global scope.

Good practice:
```scss
:global {
 #intercom-container {
   z-index: z('intercom') !important;
 }
}
```

Bad practice:
```scss
.specificContainer {
 #intercom-container {
   z-index: z('intercom') !important;
 }
}
```