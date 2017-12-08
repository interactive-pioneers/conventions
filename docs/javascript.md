# JavaScript Coding Conventions

Follow the [Google JavaScript Style Guide](https://google.github.io/styleguide/javascriptguide.xml).

## Additional Agreements

* Avoid use of anonymous functions if possible

  __good__:
  ```javascript
  function handleEvent() {
    // do something
  }

  element.on('event', handleEvent);
  ```

  __bad__:
  ```javascript
  function handleEvent() {
    //
  }

  element.on('event', function() {
    // do something
  });
  ```

## Linters

Use [JSHint](http://jshint.com/) and [JSCS](http://jscs.info/)!
Configuration files: [JSHint](https://github.com/interactive-pioneers/linter-configuration/blob/master/files/.jshintrc) | [JSCS](https://github.com/interactive-pioneers/linter-configuration/blob/master/files/.jscsrc)
