---
title: Motivation
permalink: js/motivation
layout: js
categories: js
active: js
---

At Meanbee, we have a lot of experience in both developing and maintaining Magento stores. One common problematic factor, which frequently arises during these activities, revolves around JavaScript. We have had a great deal of trouble maintaining JavaScript quite simply because it is implemented in a number of locations, including but not limited to:

- Template files
- The theme's skin directory
- The root JS directory

Frequently, these can be small functionalities. A click handler on a button, for instance, but there is no clear location to place this code. Additionally, there are a number of methods which this could be implemented; should we use the html onclick attribute? Should we use a library to attach a click handler? This document will attempt to provide a standard which considers both best development practice and ease of maintainability. 