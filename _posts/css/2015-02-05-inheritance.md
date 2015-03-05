---
title: Inheritance
permalink: css/inheritance
layout: css
categories: css
active: css
---
Inheritance should be used whenever possible to avoid declaration duplications.

{% highlight scss %}
// Instead of duplicate declarations
.promotion-banner p,
.promotion-banner h1 {
    font-size: 1.2rem;
}
{% endhighlight %}

{% highlight scss %}
// Use inheritance
.promotion-banner {
    font-size: 1.2rem;
}
{% endhighlight %}

Avoid redeclaring values when they aren't necessary:
{% highlight scss %}
// Don't do this
p {
    color: #666;
    margin: 1rem 0;
}

.parent {
    color: #000;
}

.parent p {
    color: #000;
    margin: 1rem 0 2rem;
}
{% endhighlight %}

{% highlight scss %}
// Use inheritance when possible
p {
    color: #666;
    margin: 1rem 0;
}

.parent {
    color: #000;
}

.parent p {
    color: inherit;
    margin-bottom: 2rem;
}
{% endhighlight %}