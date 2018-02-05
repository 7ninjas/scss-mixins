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
    <a href="https://7ninjas.com/careers/">Carrers</a>
    ◦
    <a href="https://7ninjas.com/contact/">Contact</a>
  </p>
</p>


## Status

[![npm](https://img.shields.io/npm/v/@7ninjas/scss-mixins.svg?style=for-the-badge)](https://www.npmjs.com/package/@7ninjas/scss-mixins)
[![npm](https://img.shields.io/npm/l/@7ninjas/scss-mixins.svg?style=for-the-badge)](https://www.npmjs.com/package/@7ninjas/scss-mixins)
[![npm](https://img.shields.io/npm/dt/@7ninjas/scss-mixins.svg?style=for-the-badge)](https://www.npmjs.com/package/@7ninjas/scss-mixins)

[![CircleCI branch](https://img.shields.io/circleci/project/github/7ninjas/scss-mixins/develop.svg?style=for-the-badge)](https://github.com/7ninjas/scss-mixins)
[![David](https://img.shields.io/david/7ninjas/scss-mixins.svg?style=for-the-badge)](https://github.com/7ninjas/scss-mixins)
[![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/7ninjas/scss-mixins.svg?style=for-the-badge)](https://github.com/7ninjas/scss-mixins)

[![GitHub issues](https://img.shields.io/github/issues/7ninjas/scss-mixins.svg?style=for-the-badge)](https://github.com/7ninjas/scss-mixins)
[![GitHub closed issues](https://img.shields.io/github/issues-closed/7ninjas/scss-mixins.svg?style=for-the-badge)](https://github.com/7ninjas/scss-mixins)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/7ninjas/scss-mixins.svg?style=for-the-badge)](https://github.com/7ninjas/scss-mixins)

[![GitHub stars](https://img.shields.io/github/stars/7ninjas/scss-mixins.svg?style=social&label=Stars&style=for-the-badge)](https://github.com/7ninjas/scss-mixins)
[![GitHub watchers](https://img.shields.io/github/watchers/7ninjas/scss-mixins.svg?style=social&label=Watch&style=for-the-badge)](https://github.com/7ninjas/scss-mixins)


## Quick start

Several quick start options are available:

- Clone the repo: `git clone https://github.com/7ninjas/scss-mixins.git`
- Install with [npm](https://www.npmjs.com/): `npm install @7ninjas/scss-mixins`
- Install with [yarn](https://yarnpkg.com/): `yarn add @7ninjas/scss-mixins`

### Usage
Import `all` file to your core `scss` file for importing all mixins from package

Example:
```scss
@import '~@7ninjas/scss-mixins/all';
```


### Table of contents

<details open>
 <summary>Animations</summary>
 
- [Full documentation](./docs/animations.md)
- [Mixin hardware](./docs/animations.md#mixin-hardware)
</details>
<details open>
  <summary>Breakpoints</summary>
  
- [Full documentation](./docs/breakpoints.md)
- [Mixin media-breakpoint-up](./docs/breakpoints.md#mixin-media-breakpoint-up)
- [Mixin media-breakpoint-down](./docs/breakpoints.md#mixin-media-breakpoint-down)
- [Mixin media-breakpoint-between](./docs/breakpoints.md#mixin-media-breakpoint-between)
- [Mixin media-breakpoint-only](./docs/breakpoints.md#mixin-media-breakpoint-only)
</details>
<details open>
  <summary>Buttons</summary>
  
- [Full documentation](./docs/buttons.md)
- [Mixin mixin-button-variant](./docs/buttons.md#mixin-button-variant)
- [Mixin mixin-button-outline-variant](./docs/buttons.md#mixin-button-outline-variant)
- [Mixin mixin-button-size](./docs/buttons.md#mixin-button-size)
</details>
<details open>
  <summary>Colors</summary>
  
- [Full documentation](./docs/colors.md)
- [Function color](./docs/colors.md#function-color)
</details>
<details open>
  <summary>Flex</summary>
  
- [Full documentation](./docs/flex.md)
- [Mixin flex](./docs/flex.md#mixin-flex)
- [Mixin inline-flex](./docs/flex.md#mixin-inline-flex)
</details>
<details open>
  <summary>Fonts</summary>
  
- [Full documentation](./docs/fonts.md)
- [Mixin font-face](./docs/fonts.md#mixin-font-face)
</details>
<details open>
  <summary>Forms</summary>
  
- [Full documentation](./docs/forms.md)
- [Mixin placeholder](./docs/forms.md#mixin-placeholder)
</details>
<details open>
  <summary>Gradients</summary>
  
- [Full documentation](./docs/gradients.md)
- [Mixin gradient-bg](./docs/gradients.md#mixin-gradient-bg)
- [Mixin gradient-x](./docs/gradients.md#mixin-gradient-x)
- [Mixin gradient-y](./docs/gradients.md#mixin-gradient-y)
- [Mixin gradient-directional](./docs/gradients.md#mixin-gradient-directional)
- [Mixin gradient-x-three-colors](./docs/gradients.md#mixin-gradient-x-three-colors)
- [Mixin gradient-y-three-colors](./docs/gradients.md#mixin-gradient-y-three-colors)
- [Mixin gradient-radial](./docs/gradients.md#mixin-gradient-radial)
- [Mixin gradient-striped](./docs/gradients.md#mixin-gradient-striped)
</details>
<details open>
  <summary>Grid</summary>
  
- [Full documentation](./docs/grid.md)
- [Mixin center](./docs/grid.md#mixin-center)
- [Mixin container](./docs/grid.md#mixin-container)
- [Mixin col](./docs/grid.md#mixin-col)
</details>
<details open>
  <summary>Hover</summary>
  
- [Full documentation](./docs/hover.md)
- [Mixin hover](./docs/hover.md#mixin-hover)
- [Mixin hover-focus](./docs/hover.md#mixin-hover-focus)
- [Mixin plain-hover-focus](./docs/hover.md#mixin-plain-hover-focus)
- [Mixin hover-focus-active](./docs/hover.md#mixin-hover-focus-active)
</details>
<details open>
  <summary>Icons</summary>
  
- [Full documentation](./docs/icons.md)
- [Mixin svg-icon](./docs/icons.md#mixin-svg-icon)
</details>
<details open>
  <summary>Images</summary>

- [Full documentation](./docs/images.md)
- [Mixin img-fluid](./docs/images.md#mixin-img-fluid)
</details>
<details open>
  <summary>Lists</summary>

- [Full documentation](./docs/lists.md)
- [Mixin list-unstyled](./docs/lists.md#mixin-list-unstyled)
</details>
<details open>
  <summary>Positioning</summary>

- [Full documentation](./docs/positioning.md)
- [Mixin size](./docs/positioning.md#function-size)
- [Mixin clearfix](./docs/positioning.md#mixin-clearfix)
- [Mixin z-index](./docs/positioning.md#mixin-z-index)
- [Mixin pseudo](./docs/positioning.md#mixin-pseudo)
- [Mixin absolute](./docs/positioning.md#mixin-absolute)
- [Mixin fixed](./docs/positioning.md#mixin-fixed)
- [Mixin relative](./docs/positioning.md#mixin-relative)
- [Mixin sticky](./docs/positioning.md#mixin-sticky)
</details>
<details open>
  <summary>Responsive</summary>

- [Full documentation](./docs/responsive.md)
- [Mixin responsive-prop](./docs/responsive.md#mixin-responsive-prop)
- [Mixin responsive-embed](./docs/responsive.md#mixin-responsive-embed)
- [Mixin responsive-col](./docs/responsive.md#mixin-responsive-col)
</details>
<details open>
  <summary>Shapes</summary>
  
- [Full documentation](./docs/shapes.md)
- [Mixin css-triangle](./docs/shapes.md#mixin-css-triangle)
</details>
<details open>
  <summary>Spacing</summary>

- [Full documentation](./docs/spacing.md)
- [Mixin ml](./docs/spacing.md#mixin-ml)
- [Mixin mt](./docs/spacing.md#mixin-mt)
- [Mixin mr](./docs/spacing.md#mixin-mr)
- [Mixin mb](./docs/spacing.md#mixin-mb)
- [Mixin mx](./docs/spacing.md#mixin-mx)
- [Mixin my](./docs/spacing.md#mixin-my)
- [Mixin m](./docs/spacing.md#mixin-m)
- [Mixin pl](./docs/spacing.md#mixin-pl)
- [Mixin pt](./docs/spacing.md#mixin-pt)
- [Mixin pr](./docs/spacing.md#mixin-pr)
- [Mixin pb](./docs/spacing.md#mixin-pb)
- [Mixin px](./docs/spacing.md#mixin-px)
- [Mixin py](./docs/spacing.md#mixin-py)
- [Mixin p](./docs/spacing.md#mixin-p)
</details>
<details open>
  <summary>Tables</summary>

- [Full documentation](./docs/tables.md)
- [Mixin table](./docs/tables.md#mixin-table)
- [Mixin table-bordered](./docs/tables.md#mixin-table-bordered)
- [Mixin table-responsible](./docs/tables.md#mixin-table-responsible)
- [Mixin table-striped](./docs/tables.md#mixin-table-striped)
- [Mixin table-hover](./docs/tables.md#mixin-table-hover)
</details>
<details open>
  <summary>Typography</summary>

- [Full documentation](./docs/typography.md)
- [Mixin text-hide](./docs/typography.md#mixin-text-hide)
- [Mixin text-truncate](./docs/typography.md#mixin-text-truncate)
- [Mixin font](./docs/typography.md#mixin-font)
</details>
<details open>
  <summary>Variables</summary>

- [Full documentation](./docs/variables.md)
</details>


## Bugs and feature requests

Found bug? Or maybe you've got great idea for feature request? Please first search for existing and closed issues.
If your problem or idea is not addressed yet - don't hesitate to [open a new issue](https://github.com/7ninjas/scss-mixins/issues/new)!


## Community

Get updates on 7ninjas's development and chat with the project maintainers and community members.

- Like [@7ninjas on Facebook](https://www.facebook.com/7ninjasHQ).
- Follow [@7ninjas on Twitter](https://twitter.com/7ninjas).
- Discover [@7ninjas Dribbble](https://dribbble.com/7ninjas)
- Explore [@7ninjas Behance](https://www.behance.net/7ninjas).
- Enjoy [@7ninjas Instagram](https://www.instagram.com/7ninjashq/).


## Versioning

To see new features and changes for each released version checkout [the Releases section of our GitHub project](https://github.com/7ninjas/scss-mixins/releases) 


## License

Code released under the MIT License.