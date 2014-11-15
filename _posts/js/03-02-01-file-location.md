---
title: File Location
permalink: js/file-location
isChild: true
layout: js
categories: js
active: js
---

There are two locations which your JavaScript should belong placed, when writing for a module. this is the `js/` directory in the root of the Magento install and somewhere in the `skin/frontend/base/default` (frontend) folder or `skin/adminhtml/default/default` (admin) folder. For the latter two, you should place all module JavaScript inside an appropriately named sub-folder here. For example, the frontend JavaScript associated with Meanbee's Postcode module should be located at `skin/frontend/base/default/js/Meanbee/Postcode/`. As an aside, we'd also advise placing CSS as another sub-folder at the same level as the `js/`.

- `js/`
	- You should place any library code, or JavaScript which you don't want to be customised or edited by the theme here. For example, if we wanted to include `underscore.js` on the page, we'd put it here.
- `skin/frontend/base/default` and `skin/adminhtml/default/default`
	- You should place any other frontend or admin JavaScript in these two locations. Note that you may (and in many cases - should!) have several files here. Lengthy, unwieldy files are a nightmare to maintain. 

As mentioned above, don't be afraid to split your code into multiple files. Provided your files are named sensibly, it makes maintenance simpler as a developer can tell where the JavaScript for a given feature / page lives at a glance. From a performance perspective this won't matter anyway, since JavaScript tends to be minified and merged in production anyway. In a similar vein, we advise a single file per class.