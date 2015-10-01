# Pure.sass

This is an unofficial port of [Pure.css](http://http://purecss.io/) framework
 to [Sass](http://sass-lang.com/). I've just copied the original source files and
 replaced some properties with variables.

The goal is to have an easily customizable version of Pure.css which fit in the Sass workflow.

It produces results seemingly identical to the original source.

## How to use

You have to import [normalize.css](https://necolas.github.io/normalize.css/) to your project.

Compiling the files will produce a file with the Pure.css default look. There are
two ways to get a custom look:

### Build a custom Pure file

Just change the value of the variables in `base/_variables.scss` and compile.

### Integrate Pure into your project style sheet

Create your custom variables file, `_custom_vars.scss`, and then import it to your
 main style sheet before pure:

```css
@import "customVariables";
@import "pure-sass/pure";
@import "yourAppStyles";
```

This will import all Pure modules into your project. You can use `base/_variables.scss`
 as a guide for customizing variables.

Import individual modules instead of `pure` if you do not want to include the whole
pure library:

```css
@import "customVariables";

/* import individual modules instead of all pure */
/* variables and base are required */
@import "pure-sass/base/variables";
@import "pure-sass/base/base";

/* let's assume we only need the grid and buttons */
@import "pure-sass/grids/grids-core";
@import "pure-sass/grids/grids-units";
@import "pure-sass/buttons/buttons-core";
@import "pure-sass/buttons/buttons";

@import "yourAppFiles";
```

Look at `pure.scss` for the available modules.

## TODO

* ~~More testing~~
* More variables
* Mixins
* Include normalize.css
* Build system based on Grunt or Gulp (or both)
