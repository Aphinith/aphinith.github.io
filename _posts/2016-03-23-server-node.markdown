---
title: "Server via Node"
layout: post
date: 2016-03-23 22:48
image: /assets/images/factorial.png
headerImage: false
tag:
- exporting modules
- server
- node
blog: true
author: aralyaphinith
description: server via node - exporting modules
---

<div class="breaker"></div>

## Exporting Modules

So there is a lot to say about servers and how they are made, but I'd like to just go over one part of it which I thought to be a really nice feature you could use to make your code look much cleaner.  It is simply the use of exporting modules from one file to another so that you just dont have one giant convoluted file of lines and lines of code.  Exporting modules allows one file to have access to features in another file with one or two simple lines of code.  For example, for the sprint we had to work on this week, we had two files: a basic-server file and a handleRequest file. We could have put everything in our basic server file, but that would have made for one file with code that doesn't necessarily need to be there.  So instead, with the use of the native features of ".exports" and "require" in node, we were able to give our basic-server file the features of the functions in our handleRequest file.

Below is the function that was in our handleRequest file and in line 46, this simple one line code will allow acces to this function in another file.

<div class="exports-image">
  <img class="image" src="../assets/images/exports.png" alt="exports file">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

Below is where we used REQUIRE in our basic-server file to gain access to the function in our handleRequest file.

<div class="require-image">
  <img class="image" src="../assets/images/require.png" alt="example of require">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

And voila!  Now our basic-server file can use the function from our handleRequest file!