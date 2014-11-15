---
title: Access to PHP values
permalink: js/access-to-php-values
isChild: true
layout: js
categories: js
active: js
---

One frequent issue which we run into is needing to access values which either exist or need to be computed in php in our JavaScript. The usual culprit is the site's base URL, often we solve this by code similar to:

{% highlight html %}
	<!-- example.phtml -->
	<h1>A title</h1>
	<p>Some markup</p>

	<script type="text/javascript">
	    var baseUrl = '<?php echo $this->getUrl('') ?>';
	</script>
{% endhighlight %}


If this value is required in a feature we could, of course, pass it as a constructor.  

There are a couple of reasons this doesn't feel like the correct way to do things:

- The JavaScript can become very difficult to read
- We could be computing the same value several times, e.g. we might have that same base URL retrieval in several locations on the site.
- It contradicts what we've said previously in this document with regards to best practice placement of JavaScript. 

One solution could be to set commonly used values in a special template file:

{% highlight html %}
<!-- javascript_globals.phtml -->

<script type="text/javascript">
if (!window.Meanbee) window.Meanbee = {};
if (!window.Meanbee.Globals) window.Meanbee.Globals = {};

window.Meanbee.Globals.baseUrl = <?php echo $this->getBaseUrl(''); ?>
...
</script>
{% endhighlight %}

In this way we are not polluting global namespace and we'll have access to these values in all our JavaScript files. 
