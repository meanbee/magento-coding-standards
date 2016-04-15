---
title: Committing Modifications
permalink: magento/committing-modifications
layout: magento
categories: magento
active: magento
---

It is common knowledge that core and community code should not be modified directly.  An extension within the local code pool should be used for such overrides.

One of the challenges when doing this is making it transparent to developers what changes have been made to the core functionality.

## Duplicate and Commit

The way that we address this problem is to commit the original code once copied to your local extension before any changes are made.  For example, if you are overriding a function, first copy and commit the function as-is.

Following this, you can then make the necessary modifications and commit. This process makes it much easier to understand what has changed by viewing the git history of this file.

The tool [DAC](https://github.com/shawesome/dac) speeds up the process of copying a template from the base theme to your custom theme and committing the initial version. There's also a handy [magerun plugin](https://github.com/meanbee/magerun-dac) to get this functionality.

There are two further steps that are recommended in making your modifications as transparent as possible:

- Add a comment to the function doc to explain what modification has been made and why. (Link to any sources for this code, e.g. stackoverflow)
- If convenient, wrap the code change in comments to mark where modifications start and end.
