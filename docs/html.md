# HTML Coding conventions

- Use semantic markup
- Use classes for styling, IDs for Javascript hooks
- If classes are used for Javascript prefix them with js- even if the result is e.g. <code class="highlight">class="portfolio__item js-portfolio__item"</code>
- __BEM Naming convention__
  BEM naming convention is used to give meaning and relations to css classes. Use in the following manner:
  - .block
  - .block__element
  - .block--modifier

  BEM modifiers are added on top of the base class e.g. <code class="highlight">class="portfolio__item portfolio__item--active</code>
  For more see [BEM explained by Harry Roberts](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/)
- __Attribute order__
  HTML attributes should follow this order for easier reading and avoiding duplicates
  - class
  - id, name
  - data-*
  - src, for, type, href, value
  - title, alt
  - aria-*, role
- __Aria-roles__
  Aria roles should be used to improve accessibility.
  This is not only applicable to the structure of a page (e.g. [Website structure with Aria roles](http://www.html5accessibility.com/tests/roles-land.html)) but also to link elements which only share a visual bond e.g. a tooltip:
{% highlight html linenos %}
<input type="text" id="password" aria-describedby="password-tip" required>
<div role="tooltip" id="password-tip">At least 8 characters long</div>
{% endhighlight %}
  For more see [MDN on ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
- __Microdata__
  Make appropriate use of microdata e.g.
{% highlight html linenos %}
<div itemscope itemtype="http://schema.org/Person">
  <a itemprop="url" href="http://www.interactive-pioneers.de"><div itemprop="name"><strong>John Doe</strong></div></a>
  <div itemscope itemtype="http://schema.org/Organization"><span itemprop="name">Interactive Pioneers</span></div>
  <div itemprop="jobtitle">Developer</div>
</div>
{% endhighlight %}
  For more see [schema.org](schema.org) and [schema creator](schema-creator.org)
