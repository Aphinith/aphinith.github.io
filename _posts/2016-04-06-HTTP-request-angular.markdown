---
title: "HTTP Request Angular"
layout: post
date: 2016-04-06 22:48
image: /assets/images/angular.png
headerImage: false
tag:
- HTTP
- API
- Angular
- Authentication Key
blog: true
author: aralyaphinith
description: HTTP Request via Angular
---

<div class="breaker"></div>

## HTTP requests with Angular to api database (with authentication key)

So I chose angular as the framework of choice for my mvp project for this sprint and I'll have to admit, so far I am loving it.  I know I'm barely skimming the surface of what this framework has to offer, but so far I am enjoying what I have seen so far.  Ok, now on to what this blog post is supposed to be about -- HTTP requests using Angular, but specifically with an authentication key from the api source.  I spent a few hours trying to figure this out (and thanks to our wonderful HIRs, we were able to figure out how to make it work).  The api database I used for my mvp is from <a href="https://theysaidso.com">theysaidso.com</a>, a database full of thousands of different kinds of quotes.  I basically just wanted to get random quotes from them.  Now there are a few ways to do this, but I'm going to only go over the three ways I tried.  All three methods should have worked, but I think something screwy was happening on their (theysaidso.com) end that prevented the first two methods from working.

The first method is to set your authentication key directly in the headers as part of your HTTP request:

<div class="angular1-image">
  <img class="image" src="../assets/images/angular1.png" alt="authentication key">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

The second method is to set $http on your module:

<div class="angular2-image">
  <img class="image" src="../assets/images/angular2.png" alt="$HTTP Request">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

The third method is to include your authentication parameters and key directly in the url.  This is also specific on how the api needs you to set it on the url as well.  This was the way I was able to make it work for this specific api:

<div class="angular3-image">
  <img class="image" src="../assets/images/angular3.png" alt="Authentication Params">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

The insertion of the authentication parameters and key comes after the '&' symbol in the above.  And there you have it folks - the three different ways to send HTTP requests with authentication keys.

<div class="breaker"></div>