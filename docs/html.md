# HTML Coding Conventions

- Use semantic markup
- Use classes for styling, IDs for Javascript hooks
- If classes are used within Javascript prefix them with `js-`
- __BEM Naming convention__ is used to give meaning and relations to css classes. Use in the following manner:
  - .block
  - .block__element
  - .block--modifier
  See also: [BEM explained by Harry Roberts](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/)
- __Attribute order__: HTML attributes should follow this order for easier reading and avoiding duplicates:
  - class
  - id, name
  - data-*
  - src, for, type, href, value
  - title, alt
  - aria-*, role
- __Aria-roles__ should be used to improve accessibility. This is not only applicable to the structure of a page (e.g. [Website structure with aria roles](http://www.html5accessibility.com/tests/roles-land.html)) but also to link elements which only share a visual bond e.g. a tooltip:

  ```html
  <input id="password" type="text" aria-describedby="password-tip" required>
  <div id="password-tip" role="tooltip">At least 8 characters long</div>
  ```
  Further reading: [MDN on ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
- __Microdata__: Make appropriate use of microdata e.g.

  ```html
  <div itemscope itemtype="http://schema.org/Person">
    <a itemprop="url" href="http://www.interactive-pioneers.de">
      <div itemprop="name"><strong>John Doe</strong></div>
    </a>
    <div itemscope itemtype="http://schema.org/Organization">
      <span itemprop="name">Interactive Pioneers</span>
    </div>
    <div itemprop="jobtitle">Developer</div>
  </div>
  ```
  See [schema.org](schema.org) and [schema creator](schema-creator.org).
