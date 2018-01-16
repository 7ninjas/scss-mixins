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

- getting started - how to create first project and, how to configure it, how to style my first component
- reboot.css or normalize.css
- help youself with <b>stylelint</b>
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
- don't style elements, style classes
- don't use id if not needed
- global styles
- styles from another packages
- creating JavaScript-specific classes to bind to, prefixed with .js-


### Nesting elements

We are pretty sure that you've heard or read tale about Little Red Riding Hood. Her mother told her to go straight way 
to Grandma's house and not stray from the path. The girl promised but soon forgot about her mother's warning. That's how she got in troubles.

With nesting elements story seems pretty the same. 

never wander too deep -> don't go more than 3 levels deep (add stylelint rule) (red hood example in being lost in code)