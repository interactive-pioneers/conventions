# Developer Conventions
Conventions for development and workflows across web application development technologies.

## VCS
### Git
1. __No mammoth commits__. Every commit should be modular and feature or fix based. Complex
commits should be avoided so producing a patch or merging code remains reasonable and inexpensive.
2. __Every commit has a comment__. If no comment comes to mind, the whole commit should be questioned. Comment requirements:
  1. Comment is written in english.
  2. Comment starts with a capital letter.
  3. Comment is meaningful and consists of more than a single word or ticket reference, e.g. `PROJECT-213` is not allowed.
  4. Comment is written in imperative, present tense to comply with internal Git style. Examples:
    - `Add green outline to submit button`
    - `Remove redundant JSON parsing method`
    - `Update README source and distribution links`
    - `Fix scrolling issue that prevents continuous scrolling of images`
  5. Comment can be followed by a longer description (or ticket reference) after the first line, separated by an empty line, e.g.:
    ``` text
    Fix scrolling issue that prevents continuous scrolling of images

    SCROLLER-123 Scrolling broken on large text areas
    http://bugs.domain.com/SCROLLER-123
    ```

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
- BEM Naming convention: `Block__Element--Modifier`
- Use classes for styling, IDs for JavaScript hooks
- Include Aria-roles

#### CSS
- Don't use spaghetti selectors e.g. `header nav ul li a`. Apply Inception rule: Never go deeper than three levels
- Don't use overly qualified selectors e.g. `.block .block__element` => `.block__element` should always reside inside `.block`
- When using calc(), add a comment on the logic behind it e.g. `calc( 100% - 5px) /* - 5px pixel to account for the border */`
- Avoid `margin-top` and `margin-bottom`. Elements should always push in one direction
- Use REMs for font declarations
- Images/icons inserted via CSS should feature a fallback text for screen readers

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
