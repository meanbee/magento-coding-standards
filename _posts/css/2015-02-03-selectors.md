---
title: Selectors
permalink: css/selectors
layout: css
categories: css
active: css
---
###Naming
Class and variable names should be lowercase and hyphen separated rather than camelcase or snakecase.
 
{% highlight scss %}
// Do not do this
.formList {}
.form_list {}
{% endhighlight %}

{% highlight scss %}
// Use hyphenated lowercase
.form-list {}
{% endhighlight %}



###ID's
Never use ID's for selectors. If you are forced to reference an ID then use an attribute selector instead. This has the same specificity as a class 
and so can be overwritten without increasing specificity levels.

{% highlight scss %}
// Never use ID selectors
#anidselector {}
{% endhighlight %}

{% highlight scss %}
// Prefer an ID attribute if it is absolutely necessary
[id='anidselector'] {}
{% endhighlight %}

###Qualifying
Never tag-qualify. By qualifying selectors specificity becomes a problem. Always rework you're markup and class structure to address inheritance issues 
instead of qualifying.

{% highlight scss %}
// Instead of this
input[type='checkbox'] {}
{% endhighlight %}

{% highlight scss %}
// Use this
[type='checkbox'] {}
{% endhighlight %}
 
###JS-Classes
Any classname prefixed with js- should not have any presentational properties attached. These are used as references for JS Classes.
Instead is- prefixed classes should be used as state classes.

{% highlight scss %}
// Don't do this
.js-navigation {
    display: block;
}
{% endhighlight %}

{% highlight scss %}
// Use this
.is-active {
    &.navigation {
        display: block;
    }
}
{% endhighlight %}

This allows for the removal of JS without interfering with presentation.