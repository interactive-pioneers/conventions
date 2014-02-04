# Developer Conventions
Conventions for development and workflows across web application development technologies.

## VCS
### Git
1. __No mammoth commits__. Every commit should be modular and feature or fix based. Complex
commits should be avoided so producing a patch or merging code remains reasonable and inexpensive.
2. __Every commit has a comment__. If no comment comes to mind, the whole commit should be questioned. Comment requirements:
  1. Comment starts with a capital letter.
  2. Comment is meaningful and consists of more than a single word or ticket reference, e.g. `PROJECT-213` is not allowed.
  3. Comment is written in imperative, present tense to comply with internal Git style. Examples:
    - `Add green outline to submit button`
    - `Remove redundant JSON parsing method`
    - `Update README source and distribution links`
    - `Fix scrolling issue that prevents continuous scrolling of images`
  4. Comment can be followed by a longer description (or ticket reference) after the first line, separated by an empty line, e.g.:
    ``` text
    Fix scrolling issue that prevents continuous scrolling of images

    SCROLLER-123 Scrolling broken on large text areas
    http://bugs.domain.com/SCROLLER-123
    ```   

## Coding conventions

Coding conventions for various technologies and frameworks follow the generic industry standard, i.e. those defined by the maintaining organisation or community.

__Basic concepts__:
- __DRY__. Don't Repeat Yourself.
- __Readability__.
- __Seamless formatting__. No formatting variability across a project.

### Front-end
#### HTML
_Coming soon_
#### CSS
_Coming soon_
#### JavaScript
_Coming soon_

### Backend
#### PHP
_Coming soon_
#### Ruby
_Coming soon_
