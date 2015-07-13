---
layout: page
title: SCSS Guidelines
permalink: /guidelines/scss/index.html
---

These are the practices I do my best to follow when writing SCSS. As with the rest of the guidelines here, even though this is how I normally want to write SCSS, it is always better to have guidelines like this for your team that everyone follows.

## Syntax
<div class="section" markdown="1">
<div class="description" markdown="1">
* Use soft tabs four spaces - this ensures that the code looks identical in all editors. I use four spaces instead of two because it makes the levels much clearer.
* Have each selector in a selector group on a separate line. The comma between selectors should be placed on the end of the upper line.
* Have the opening brace on the same line as the selector, separated with one space.
* Have the closing brace on a new line.
* Don't use any space before the `:` in a declaration.
* Use one space after the `:` in a declaration.
* Always end a declaration with a `;`. 
* For multi-value declarations (e.g. `box-shadow`), separate the values with comma followed by a new line. The lines should be indented so all values are aligned.
* Don't specify unit for zero values.
* Use `hsl()` colors instead of hex or `rgb()`. I find HSL to be more intuitive when modifying the colors programatically.
* Use `hsla()` only when you need to define an alpha value.
* Don't use color aliases. Nope, none of them, not even <span markdown="1" style="color: papayawhip">`papayawhip`</span> or <span markdown="1" style="color: peachpuff">`peachpuff`</span>.
* Don't use spaces on either side of the comma in functions (e.g. `hsl()`). This helps to identify them as one value as opposed from multi-value declarations.
</div>

{% highlight scss %}
// Bad
.selector1, .selector2{
    display : inline-block;
    box-shadow: 0px 2px #000, inset 0px 1px white;
}


// Good
.selector1,
.selector2 {
    display: inline-block;
    box-shadow: 0 2px hsl(0,0%,0%),
                inset 0 1px hsl(0,0%,100%);
}
{% endhighlight %}
</div>

## Selectors

<div class="section" markdown="1">
<div class="description" markdown="1">
* Always strive to keep the specificity as low as possible. This makes the styles more maintainable, and enables a better flow from general styles towards more specific styles. 
* Don't use IDs when styling. They no longer provide any notable performance benefit over classes, they only increase the specificity of your selector.
* Use element selectors only for base styles. Use classes when you need to get more specific than that. Classes better describe the intent you are trying to convey, while the intent of an element can be very vague.
* Introduce new classes instead of long selectors.
</div>

{% highlight scss %}
// Bad
#nav {}
#nav > ul > li > a {}
.content-wrapper > div {}

// Good
.nav {}
.nav-link {}
.content {}

{% endhighlight %}
</div>

## Naming

<div class="section" markdown="1">
<div class="description" markdown="1">

</div>

{% highlight scss %}

{% endhighlight %}
</div>

## Vendor prefixes

<div class="section" markdown="1">
<div class="description" markdown="1">
Use Autoprefixer. 

Or Prefixfree. 

Or whatever tool you like that does the job, but don't do it yourself. Vendor prefixes makes the code harder to read and creates noice when only very few of the declarations are actually used by any single browser. 

Besides, who remembers every vendor prefix and keeps up to date when they can be dropped? Well, an automated tool does, so use it!
</div>

{% highlight scss %}
// Bad
.selector {
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack:         stretch;
  -webkit-justify-content:  stretch;
      -ms-flex-pack:        stretch;
          justify-content:  stretch;
}

// Good
.selector {
    display: flex;
    justify-content: stretch;
}

{% endhighlight %}
</div>

## Nesting

<div class="section" markdown="1">
<div class="description" markdown="1">
</div>

{% highlight scss %}

{% endhighlight %}
</div>

## File structure

<div class="section" markdown="1">
<div class="description" markdown="1">
</div>

{% highlight scss %}

{% endhighlight %}
</div>




