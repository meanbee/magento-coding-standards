---
title: Commit Messages
permalink: tools/commit-messages
layout: tools
categories: tools
active: tools
---

The first line of a git commit message should be a short summary of changes and should be 50 characters or less. You should keep it concise, but clear. If your change is related to a ticket, you should include a ticket id or reference at the beginning of the message, so it is visible when viewing a list of commits.

If you feel that the commit needs a longer explanation, leave a blank line after the first line and then organise the rest of the message into paragraphs (or bullet point lists), wrapped at 72 characters. Imagine the first line as the subject of the commit while the rest of it as the message. It is a good idea to configure your git message editor to automatically format commit messages for you and warn you when you are breaking the format.

When writing commit messages, you should use the imperative and present tense. This matches the format of the commit messages that git automatically generates.

Example commit message:

<pre>
MB-49: Add git standards

Include commit message standards based on popular git commit message
guidelines and branching standards based on our workflow.
</pre>

For more information and explanations of the reasons behind these standards, you can read [this article](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html).
