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
* Have the opening brace on the same line as the selector, separated with one space.
* Have the closing brace on a new line.
* Don't use any space before the `:` in a declaration.
* Use one space after the `:` in a declaration.
* Have each selector in a selector group on a separate line. The comma between selectors should be placed on the end of the upper line.
</div>

{% highlight scss %}
// Bad
.selector1, .selector2{
    display :inline-block;
}


// Good
.selector1,
.selector2 {
    display: inline-block;
}
{% endhighlight %}
</div>

## Naming


