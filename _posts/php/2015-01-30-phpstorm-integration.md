---
title: PHPStorm Integration
permalink: php/phpstorm-integration
layout: php
categories: php
active: php
---

Most of our developers use [PHPStorm](https://www.jetbrains.com/phpstorm/) as their IDE, so we have created the [Meanbee.xml](/assets/php/Meanbee.xml) code style scheme to keep our IDE settings consistent. To use it, place the xml file inside the *config/codestyles* directory under the [PHPStorm home directory](https://www.jetbrains.com/phpstorm/help/project-and-ide-settings.html#d739710e149) and enable it in *Preferences > Editor > Code Style*.

We also have our PHPStorm configured to run *PHP_CodeSniffer* to highlight any coding style issues. To set it up, you can follow [this tutorial](http://rob3000.com/installing-magento-code-sniffer/), which also provides Code Sniffer standards for Magento 1.
