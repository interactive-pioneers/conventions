# SCSS Coding conventions

- Configuration: [.scss-lint.yml](/files/.scss-lint.yml) for [scss-lint](https://github.com/brigade/scss-lint)
- Full documentation: [scss-lint](https://github.com/brigade/scss-lint/blob/master/lib/scss_lint/linter/README.md)
- Disabling linters:
  - [Documentation](https://github.com/brigade/scss-lint#disabling-linters-via-source)
  - If you can't avoid an error add an inline or a file width exception and document why you added it.

# CSS Coding conventions

- Don't use spaghetti selectors e.g. `header nav ul li a`. NEVER go deeper than three levels!
- Don't use overly qualified selectors e.g. `.block .element` => `.block__element` should always reside inside <code class="highlight">.block<code class="highlight">
- When using calc(), add a comment on the logic behind it e.g. `width: calc(100% - 5px) /* - 5px pixel to account for the border */`
- Avoid `margin-top` and `margin-bottom` on the same element. Elements should always push in one direction (preferably downwards)
- Use REMs for font declarations
- Use em unit (which is relative to the font-size) only where the given property really has a fixed relation to the element font-size defined by the design, otherwise use pixel (px) values
- Images/icons inserted via CSS should feature a fallback text for screen readers
- Single line declarations should only be used for a single value
- For information on BEM see [HTML](/HTML)
  ```css
  /* correct */
  body { background: white; }
  /* false */
  body { background: white; color: black; }
  ```
- __Structure__
  CSS is structured in the following folders: (as per [Harry Roberts ITCSS](http://itcss.io))
  1. __Settings__: Global variables, config switches
  2. __Tools__: Default mixins and functions
  3. __Generic__: Ground-zero styles (Normalize.css, resets, box-sizing)
  4. __Base__: Unclassed HTML elements (type selectors)
  5. __Objects__: Cosmetic-free design patterns
  6. __Components__: Designed components, chunks of UI
  7. __Trumps__: Helpers and overrides
- __Declaration order__ (as per [Nicolas Gallagher's Idiomatic CSS](https://github.com/necolas/idiomatic-css))
  1. Positioning
  2. Display, Layout Modes & Box Model
  3. Visual Styles
  4. Text Styles
  5. Transforms
  6. Transitions and Animations
  7. Browser UI
  8. Other

A tool that can be used to automatically manage declaration order is [CSScomb](http://csscomb.com/)

```css
.selector {
  /* Positioning */
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 10;

  /* Display & Box Model */
  display: inline-block;
  overflow: hidden;
  box-sizing: border-box;
  margin: 10px;
  padding: 10px;
  width: 100px;
  height: 100px;
  border: 10px solid #333;

  /* Visual Styles */
  visibility: visible;
  opacity: 1;
  border-radius: none;
  border-image: none;
  outline: none;
  background: #000;
  box-shadow: none;
  filter: none;

  /* Text Styles */
  color: #fff;
  font-family: sans-serif;
  font-size: 16px;
  line-height: 1;
  vertical-align: baseline;
  direction: ltr;
  text-align: right;

  /* Transforms */
  transform: none;
  perspective: none;
  backface-visibility: hidden;

  /* Transitions and Animations */
  transition: none;
  animation: none;
}
```

- __Nesting in preprocessors__
  1. Remember not to nest deeper than three levels
  2. Leave an empty line between a rule and a nested element

```css
.modal {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;

  display: none;

  &__open {
    display: block;
  }
}
```