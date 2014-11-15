---
title: File Location
permalink: js/file-location
isChild: true
layout: js
categories: js
active: js
---


Much of what was said in Module Development applies to theme development; Place any libraries in `js/` and place your theme specific JavaScript in the `skin/` subdirectory. The one addition, for `frontend` development, is that it shouldn't be inside `skin/frontend/base/default/js` but inside `skin/frontend/your_package/your_theme/js` instead. 

We suggest the following file structure when you begin theme development

	global.js
	product.js
	category.js
	home.js
	checkout.js
	... (any other high level files)
	lib/

Where JavaScript for all pages (equivalent to the default handle in Magento) goes in `global.js` and specific JavaScript to each page goes into the obvious files. You may wish to add more js files here, but that depends on your project. These files should contain things minor JavaScript, behavioural tweaks. Things like click handlers, page onload animations; generally code that doesn't belong as part of a larger feature, or isn't reusable across other pages.

One point I'd like to stress regarding things like click handlers is to provide an easy route to trace this behaviour from the markup. At Meanbee, we've run into several problems we return to a project to perform some maintenance and it's a mystery what JavaScript is manipulating a page. Therefore our simple solution is just to place a PHP comment in the template describing what JavaScript is affecting the markup and where it can be found. 

Features can be placed in a folder hierarchy in the lib folder, for instance let's say we have a class Meanbee.Core.Calendar. We would place the JavaScript file in `lib/Meanbee/Core/Calendar.js`. We can then instantiate the class in a template or in one of the top level JavaScript files. 
