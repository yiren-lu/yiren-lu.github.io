---
layout: page
title: Board 2
description: a private markdown persistent pastebin
img: /assets/img/ot.png
importance: 1
category: work
---

Board 2 presents a convenient Pastebin service, which can be of great help when you want to share some snippet of text with your friend. You can simply paste a markdown snippet, obtain a URL pointing to the document, and send it to your friend.

It is integrated with a markdown renderer that supports latex formula rendering and source code syntax highlighting in addition to standard markdown features. Moreover, it offers a pretty and user-friendly two-column online markdown editor, where you can edit your markdown content on the left side and preview rendered results on the right side, and the two columns will scroll to some proper position in accordance with one another.

What makes it more powerful than most common Pastebin services is that it offers two types of URLs, one for readers and one for writers. That is, through the reader's URL, one can only read the rendered HTML result, but users with the URL for writers are able to edit the raw markdown snippets as well. And synchronous editing introduces new trouble, that when multiple edits are created by different users simultaneously, how can we properly merge the change events and present all users with the same ultimate result? The solution is operational transformation.

In Board 2, all edits users make are treated as operations like `inserting a string s after position p` or `delete p characters starting from position p`. And for each client, all edits together form a sequence of operations. 

