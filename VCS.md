# Version Control

## Git

1. Setup
  1. Please add your full name to your git credentials: [set up git](https://help.github.com/articles/set-up-git/)

### Commits

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

### No-commits

1. Passwords unless harmless
2. IDE metadata, e.g. `/nbproject` for NetBeans
3. Runtime data, e.g. `wp-content/uploads` for Wordpress

### Branching

1. Every feature should be developed in its own feature branch referring:
  1. to feature;
  2. to ticket number involved
  e.g. `feature/advanced-combobox-<ticket number>`
2. Every fix should be developed in its own fix branch, similarly to pt. 1, e.g. `fix/combobox-visual-flaw-<ticket number>`
3. Every feature and fix branch should be deleted locally and remotely as soon as the related ticket is closed

### Tagging

1. __Every release has a tag__. No release is made without a tag. Every current and future member of the team needs to be able to identify what was the exact state of the release.
2. __Tags are _semver_ compatible__. All tags follow [Semantic Versioning](http://semver.org). For example: `v0.1.2` or `v1.2.13`. Increasing a version number should depend on the nature of the update as by the concepts of _semver_ and is extremely important for software that can become a dependency (RubyGems, Bower, NPM, etc.). __Incorrect versioning of a library could break software that is depending on it!__
3. __Prerelease tagging is OK__. If you're not sure about the release and it needs additional evaluation, use a suffix so it becomes self-explanatory, e.g. `v1.2.3-a1`, `v0.2.4-b2`, `v2.2.9-rc3` for Alpha 1, Beta 2, Release Candidate 3, respectively.
