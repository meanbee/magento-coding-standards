---
title: Legacy Browsers
permalink: css/legacy-browsers
layout: css
categories: css
active: css
---
Sass allows handling of legacy browser specific css without the use of hacks. Hacks should never be used under
any circumstance. For old IE browser versions, a separate css file should be created with fallbacks. This
ensures that modern browsers are not populated with unnecessary declarations. In Sass projects use the
IE mixin:

{% highlight scss %}
.selector {
    background-color: rgba(255, 255, 255, .6);
    
    @include before-ie-9 {
        background-image: url('images/white-transparency-60.png');
    }
}
{% endhighlight %}