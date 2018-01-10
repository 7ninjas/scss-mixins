<p align="center">
  <a href="https://7ninjas.com/">
    <img src="https://getbootstrap.com/assets/brand/bootstrap-solid.svg" alt="" width=72 height=72>
  </a>

  <h3 align="center">7ninjas</h3>

  <p align="center">
    `scss-mixins` is a collection of scss mixins and functions to ease and improve implementations of common style-code patterns.
    <br>
    <a href="https://getbootstrap.com/docs/4.0/"><strong>Discover Scss Mixins docs »</strong></a>
    <br>
    <br>
    <a href="https://7ninjas.com/case-studies/">Portfolio</a>
    ·
    <a href="https://7ninjas.com/careers/">Carrers</a>
    ·
    <a href="https://7ninjas.com/contact/">Contact</a>
  </p>
</p>


### Table of contents

- [Animations](./docs/animations.md)
- [Base](./docs/base.md)
- [Breakpoints](./docs/breakpoints.md)
- [Colors](./docs/colors.md)
- [Flex](./docs/flex.md)
- [Fonts](./docs/fonts.md)
- [Forms](./docs/forms.md)
- [Gradients](./docs/gradients.md)
- [Grid](./docs/grid.md)
- [Hover](./docs/hover.md)
- [Icons](./docs/icons.md)
- [Images](./docs/images.md)
- [Lists](./docs/lists.md)
- [Responsive](./docs/responsive.md)
- [Shapes](./docs/shapes.md)
- [Spacing](./docs/spacing.md)
- [Transitions](./docs/transitions.md)
- [Typography](./docs/typography.md)
- [Units](./docs/units.md)
- [Utils](./docs/utils.md)
- [Variables](./docs/variables.md)


## Quick start

Several quick start options are available:

- Clone the repo: `git clone https://github.com/7ninjas/scss-mixins.git`
- Install with [npm](https://www.npmjs.com/): `npm install @7ninjas/scss-mixins`
- Install with [yarn](https://yarnpkg.com/): `yarn add @7ninjas/scss-mixins`


## Status

[![npm](https://img.shields.io/npm/v/npm.svg?style=for-the-badge)](https://www.npmjs.com/package/@7ninjas/scss-mixins)
[![npm](https://img.shields.io/npm/l/express.svg?style=for-the-badge)](https://github.com/7ninjas/scss-mixins)

[![GitHub stars](https://img.shields.io/github/stars/badges/shields.svg?style=social&label=Stars&style=for-the-badge)](https://github.com/7ninjas/scss-mixins)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/cdnjs/cdnjs.svg?style=for-the-badge)](https://github.com/7ninjas/scss-mixins)
[![GitHub issues](https://img.shields.io/github/issues/badges/shields.svg?style=for-the-badge)](https://github.com/7ninjas/scss-mixins)

[![David](https://img.shields.io/david/expressjs/express.svg?style=for-the-badge)](https://github.com/7ninjas/scss-mixins)


[![devDependency Status](https://img.shields.io/david/dev/twbs/bootstrap.svg)](https://david-dm.org/twbs/bootstrap?type=dev)
[![CSS gzip size](http://img.badgesize.io/twbs/bootstrap/v4-dev/dist/css/bootstrap.min.css?compression=gzip&label=CSS+gzip+size)](https://github.com/twbs/bootstrap/tree/v4-dev/dist/css/bootstrap.min.css)
[![JS gzip size](http://img.badgesize.io/twbs/bootstrap/v4-dev/dist/js/bootstrap.min.js?compression=gzip&label=JS+gzip+size)](https://github.com/twbs/bootstrap/tree/v4-dev/dist/js/bootstrap.min.js)

## What's included

Within the download you'll find the following directories and files, logically grouping common assets and providing both compiled and minified variations. You'll see something like this:

```
bootstrap/
├── css/
│   ├── bootstrap.css
│   ├── bootstrap.css.map
│   ├── bootstrap.min.css
│   ├── bootstrap.min.css.map
│   ├── bootstrap-grid.css
│   ├── bootstrap-grid.css.map
│   ├── bootstrap-grid.min.css
│   ├── bootstrap-grid.min.css.map
│   ├── bootstrap-reboot.css
│   ├── bootstrap-reboot.css.map
│   ├── bootstrap-reboot.min.css
│   └── bootstrap-reboot.min.css.map
└── js/
    ├── bootstrap.bundle.js
    ├── bootstrap.bundle.min.js
    ├── bootstrap.js
    └── bootstrap.min.js
```

We provide compiled CSS and JS (`bootstrap.*`), as well as compiled and minified CSS and JS (`bootstrap.min.*`). CSS [source maps](https://developers.google.com/web/tools/chrome-devtools/debug/readability/source-maps) (`bootstrap.*.map`) are available for use with certain browsers' developer tools. Bundled JS files (`bootstrap.bundle.js` and minified `bootstrap.bundle.min.js`) include [Popper](https://popper.js.org/), but not [jQuery](https://jquery.com/).


## Bugs and feature requests

Have a bug or a feature request? Please first read the [issue guidelines](https://github.com/twbs/bootstrap/blob/master/CONTRIBUTING.md#using-the-issue-tracker) and search for existing and closed issues. If your problem or idea is not addressed yet, [please open a new issue](https://github.com/twbs/bootstrap/issues/new).


## Documentation

Bootstrap's documentation, included in this repo in the root directory, is built with [Jekyll](https://jekyllrb.com/) and publicly hosted on GitHub Pages at <https://getbootstrap.com/>. The docs may also be run locally.

Documentation search is powered by [Algolia's DocSearch](https://community.algolia.com/docsearch/). Working on our search? Be sure to set `debug: true` in the `_scripts.html` include.

### Running documentation locally

1. Run through the [tooling setup](https://getbootstrap.com/docs/4.0/getting-started/build-tools/#tooling-setup) to install Jekyll (the site builder) and other Ruby dependencies with `bundle install`.
2. Run `npm install` to install Node.js dependencies.
3. Run `npm run test` (or a specific NPM script) to rebuild distributed CSS and JavaScript files, as well as our docs assets.
4. From the root `/bootstrap` directory, run `npm run docs-serve` in the command line.
5. Open `http://localhost:9001` in your browser, and voilà.

Learn more about using Jekyll by reading its [documentation](https://jekyllrb.com/docs/home/).

### Documentation for previous releases

- For v2.3.2: <https://getbootstrap.com/2.3.2/>
- For v3.3.x: <https://getbootstrap.com/docs/3.3/>

[Previous releases](https://github.com/twbs/bootstrap/releases) and their documentation are also available for download.


## Contributing

Please read through our [contributing guidelines](https://github.com/twbs/bootstrap/blob/master/CONTRIBUTING.md). Included are directions for opening issues, coding standards, and notes on development.

Moreover, if your pull request contains JavaScript patches or features, you must include [relevant unit tests](https://github.com/twbs/bootstrap/tree/master/js/tests). All HTML and CSS should conform to the [Code Guide](https://github.com/mdo/code-guide), maintained by [Mark Otto](https://github.com/mdo).

Editor preferences are available in the [editor config](https://github.com/twbs/bootstrap/blob/master/.editorconfig) for easy use in common text editors. Read more and download plugins at <http://editorconfig.org/>.


## Community

Get updates on Bootstrap's development and chat with the project maintainers and community members.

- Follow [@getbootstrap on Twitter](https://twitter.com/getbootstrap).
- Read and subscribe to [The Official Bootstrap Blog](https://blog.getbootstrap.com/).
- Join [the official Slack room](https://bootstrap-slack.herokuapp.com/).
- Chat with fellow Bootstrappers in IRC. On the `irc.freenode.net` server, in the `##bootstrap` channel.
- Implementation help may be found at Stack Overflow (tagged [`bootstrap-4`](https://stackoverflow.com/questions/tagged/bootstrap-4)).
- Developers should use the keyword `bootstrap` on packages which modify or add to the functionality of Bootstrap when distributing through [npm](https://www.npmjs.com/browse/keyword/bootstrap) or similar delivery mechanisms for maximum discoverability.


## Versioning

For transparency into our release cycle and in striving to maintain backward compatibility, Bootstrap is maintained under [the Semantic Versioning guidelines](http://semver.org/). Sometimes we screw up, but we'll adhere to those rules whenever possible.

See [the Releases section of our GitHub project](https://github.com/twbs/bootstrap/releases) for changelogs for each release version of Bootstrap. Release announcement posts on [the official Bootstrap blog](https://blog.getbootstrap.com/) contain summaries of the most noteworthy changes made in each release.


## Creators

**7ninjas**

- <https://www.facebook.com/7ninjasHQ>
- <https://twitter.com/7ninjas>
- <https://www.linkedin.com/company/7ninjas>
- <https://www.instagram.com/7ninjashq/>
- <https://dribbble.com/7ninjas>
- <https://www.behance.net/7ninjas>


## License

Code released under the [MIT License](https://github.com/twbs/bootstrap/blob/master/LICENSE).





[![npm version](https://badge.fury.io/js/%407ninjas%2Fscss-mixins.svg)](https://badge.fury.io/js/%407ninjas%2Fscss-mixins)

### Description
`scss-mixins` is a collection of scss mixins and functions to ease and improve implementations of common style-code patterns.

### Usage
Import this file to your core `scss` file for importing all mixins from package

Example:
```scss
@import '~scss-mixins/components/base'
```
