# JavaScript

- [JSHint](http://jshint.com/) and [JSCS](http://jscs.info/) for quality control
- Follow the [Google style guide](https://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml)

In addition to [Google style guide](https://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml), following conventions are respected:

## `var` declarations

- Consecutive declarations with tabulation recommended

```js
var something     = '';
var somethingElse = null;
var andYetAnother = null;
```

- Comma-separated declarations correctly indented and with tabulation recommended

```js
var something                  = '',
    somethingElse              = null,
    andYetAnotherCommaFollower = null;
```

On Vim, [tabular](https://github.com/godlygeek/tabular) can be used to easily achieve the acceptable tabulation.