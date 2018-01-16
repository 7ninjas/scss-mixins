# variables.scss.example

This file includes all variables used in all mixins from `src` folder.   
If you want to include all mixins from this package to your project, you should take some steps:
- import `_all.scss` file from package root directory to your core scss file.
    ```scss
    @import '~@7ninjas/scss-mixins/all';
    ```
- copy `_variables.scss.example` file from package root directory to your project and rename it to `_variables.scss` 
- import `_variables.scss` to your core scss file
- change variables in `_variables.scss` if needed
