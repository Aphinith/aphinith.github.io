---
title: "Recursion"
layout: post
date: 2016-03-04 22:48
image: /assets/images/factorial.png
headerImage: false
tag:
- markdown
- components
- extra
blog: true
author: aralyaphinith
description: Factorial with recursion
---

## Practice Makes Perfect

<span class="evidence">I have to admit, the first time recursion was introduced to me, I was very confused as to what this even was.  Though at the time, I was also having difficulty wrapping my head around passing in functions as arguments in another function.  After further study and exposure to more javascript, I can confidently say that I understand the basic concept of recursion.  It is basically calling itself within itself recursively to achieve the desired end result.  Now keep in mind understanding this core concept is much different from putting it down in code to achieve this.  I still have issues as to when to apply recursion within the code depending on how complicated the code is.  But just like anything out there, practice makes perfect.</span>

## Factorial

<span class="evidence">The below example was a good introduction to recursion for me.  A factorial function used to call itself recursively: </span>

<div class="factorial">
  <img class="image" src="{{ site.url }}/{{ site.picture }}" alt="factorial function">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

<span class="evidence">Every recursive function will have at least one base case to end the recursion.  In the above case, once the 'number' reaches 0, the function will no longer call itself and just return 1. -- Friday, March 4th, 2016</span>







