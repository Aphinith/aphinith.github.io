---
title: "Sending HTTP Requests Server Side"
layout: post
date: 2016-08-21 22:48
image: 
headerImage: false
tag:
- HTTP
- RESTful
- Heroku
- API
blog: true
author: aralyaphinith
description: Handling HTTP requests from the server side
---

<div class="breaker"></div>

## Why setup HTTP request on the server side you ask?

Well I ran into some trouble with one of my deployed apps on Heroku. It wouldn't allow for me to make an HTTP request to the api I was using because the request needed to be a secure request, which needed to be an HTTPS type protocol. Also, I was making this request from the front end component, which is also why it didn't work. If the url you are using to make the api call uses a secure HTTPS request, then you wont need to worry about this, but if it isn't a secure request, then you must handle these calls on the server side.

## Setup your server file

First you will need to get the [request](https://www.npmjs.com/package/request) package from npm. In your terminal type in

{% highlight html %}
npm install --save request
{% endhighlight %}

Your package.json file should now have request as one of your dependencies. Make sure you update your node modules folder with

{% highlight html %}
npm update
{% endhighlight %}

Now in your server.js (or index.js) file, make sure you require the 'require' module.
 
<div class="require-request">
  <img class="image" src="../assets/images/HTTP1.png" alt="process.env.PORT">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

And it is as simple as that. Below is an example of how to make a GET request to an api. The request call takes two arguments, the first argument is the url for the http requests, the second argument is a function that takes three parameters: error, response, and body. 

<div class="making-request">
  <img class="image" src="../assets/images/HTTP2.png" alt="package.json file">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

If you'd like to read more on making POSTS or PUT or any other types of RESTful calls, read the docs on [Request Here](https://www.npmjs.com/package/request).
