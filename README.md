# Developer Conventions
Conventions for development and workflows across web application development technologies.

- [Version Control](VCS.md)

## Coding conventions

Coding conventions for various technologies and frameworks follow the generic industry standard, i.e. those defined by the maintaining organisation or community.

__Basic concepts__:
- __DRY__. Don't Repeat Yourself.
- __Modular & reusable__.
- __Readability__.
- __Seamless formatting__. No formatting variability across a project.

### Front-end
#### HTML
- Use semantic markup
- Use classes for styling, IDs for JavaScript hooks
- __BEM Naming convention__
  BEM naming convention is used to give meaning and relations to css classes. Use in the following manner:
  - `.block`
  - `.block__element`
  - `.block--modifier`

  E.g. `<div class="portfolio__entry portfolio__entry--active"></div>`
  For more see [BEM explained by Harry Roberts](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/)
- __Attribute order__
  HTML attributes should follow this order for easier reading and avoiding duplicates
  - `class`
  - `id, name`
  - `data-*`
  - `src, for, type, href, value`
  - `title, alt`
  - `aria-*, role`
- __Aria-roles__
  Aria roles should be used to improve accessibility.
  This is not only applicable to the structure of a page (e.g. [Website structure with Aria roles](http://www.html5accessibility.com/tests/roles-land.html)) but also to link elements which only share a visual bond e.g. a tooltip:
  `<input type="text" id="password" aria-describedby="password-tip" required>`
  `<div role="tooltip" id="password-tip">At least 8 characters long</div>`
  For more see [MDN on ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
- __Microdata__
  Make appropriate use of microdata e.g.
  `<div itemscope itemtype="http://schema.org/Person">`
  &nbsp;&nbsp;`<a itemprop="url" href="http://www.interactive-pioneers.de"><div itemprop="name"><strong>John Doe</strong></div></a>`
  &nbsp;&nbsp;`<div itemscope itemtype="http://schema.org/Organization"><span itemprop="name">Interactive Pioneers</span></div><div itemprop="jobtitle">Developer</div>`
  `</div>`
  For more see [schema.org](schema.org) and [schema creator](schema-creator.org)

#### CSS
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

#### JavaScript
- `'use strict';` mode
- Use JSHint for linting
- Use inline comments where it's sensible, block comments for functions and plugins
- Always use closure

### Backend
#### PHP
_Coming soon_
#### Ruby
_Coming soon_