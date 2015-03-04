# CSS Coding Convention

- Don't use spaghetti selectors e.g. `header nav ul li a`. Apply Inception rule: Never go deeper than three levels
- Don't use overly qualified selectors e.g. `.block .block__element` => `.block__element` should always reside inside `.block`
- When using calc(), add a comment on the logic behind it e.g. `calc( 100% - 5px) /* - 5px pixel to account for the border */`
- Avoid `margin-top` and `margin-bottom` on the same element. Elements should always push in one direction (preferably downwards)
- Use REMs for font declarations
- Images/icons inserted via CSS should feature a fallback text for screen readers
- __Structure__
  CSS is structured in the following folders: (as per [Harry Roberts ITCSS](itcss.io))
  1. __Settings__: Global variables, config switches
  2. __Tools__: Default mixins and functions
  3. __Generic__: Ground-zero styles (Normalize.css, resets, box-sizing)
  4. __Base__: Unclassed HTML elements (type selectors)
  5. __Objects__: Cosmetic-free design patterns
  6. __Components__: Designed components, chunks of UI
  7. __Trumps__: Helpers and overrides
- __Declaration order__ (as per [Nicolas Gallagher's Idiomatic CSS](https://github.com/necolas/idiomatic-css))
  1. Positioning
  2. Display & Box Model
  3. Other