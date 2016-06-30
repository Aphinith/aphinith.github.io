---
title: "Recursion"
layout: post
date: 2016-03-04 22:48
image: /assets/images/factorial.png
headerImage: false
tag:
- recursion
- scope
blog: true
author: aralyaphinith
description: Factorial with recursion
---

<div class="breaker"></div>

## Practice Makes Perfect

I have to admit, the first time recursion was introduced to me, I was very confused as to what this even was.  Though at the time, I was also having difficulty wrapping my head around passing in functions as arguments in another function.  After further study and exposure to more javascript, I can confidently say that I understand the basic concept of recursion.  It is basically calling itself within itself recursively to achieve the desired end result.  Now keep in mind understanding this core concept is much different from putting it down in code to achieve this.  I still have issues as to when to apply recursion within the code depending on how complicated the code is.  But just like anything out there, practice makes perfect.

## Factorial

The below example was a good introduction to recursion for me.  A factorial function used to call itself recursively:

<div class="factorial">
  <img class="image" src="../assets/images/factorial.png" alt="factorial function">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

Every recursive function will have at least one base case to end the recursion.  In the above case, once the 'number' reaches 0, the function will no longer call itself and just return 1.

<div class="breaker"></div>







