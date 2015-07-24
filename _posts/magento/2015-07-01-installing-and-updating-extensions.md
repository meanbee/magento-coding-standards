---
title: Installing and Updating Extensions
permalink: magento/installing-and-updating extensions
layout: magento
categories: magento
active: magento
---

## Installation

Unless otherwise dictated by project standards, Magento extensions should always be installed
fully and committed to the respository. Symlinks or composer dependencies should not be used. This
makes deployments easier and allows the store to continue working in case a dependency disappears.

Preferred extension installation methods are:

- Modman installation (`modman clone --copy https://github.com/example/extension.git`)
- Magento command line installation (`./mage install-file Extension.tgz`)
- Manual copy of extension files

## Commits

Installed extensions must be committed to the repository as a single atomic commit. Any modifications
or theme customisations should follow in separate commits.

The extension name and version should be included in the commit message. This allows for an easy
audit by looking at the commit history without having to review the codebase. For example:

    ISSUE-123: Install Meanbee_Royalmail v2.6.5

Extension source files, such as the .tgz file or .modman directory, should not be committed.

## Upgrades

When upgrading extensions, follow the same installation procedure as for new extensions.

If the extension is being upgraded by manually extracting the new files, it is safer to delete the
existing extension directories before copying new files. This ensures that the files removed in the
new version of the extension are removed from the repository as well, instead of merging the existing
set of files with the new set.

Extension upgrades must be committed to the repository as a single atomic commit and must include the
extension name and the new version in the commit message. Including the old version of the extension
in the commit message is optional, but can be useful for audit purposes. For example:

    ISSUE-123: Update Meanbee_Royalmail to v2.6.5

    Previously was v2.5.3.

If any changes are required to the extension or theme customisations in order to retain the compatibility
of the extension with the store after the upgrade, they can be committed in the same commit as the upgrade
itself. This is in order to preserve a working state of the extension before and after the upgrade commit.
However, if the amount of customisations is extensive or is related to setting up new features, then separate
follow up commits are advisable.

