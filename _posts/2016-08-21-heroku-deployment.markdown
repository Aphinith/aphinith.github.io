---
title: "Deployment with Heroku"
layout: post
date: 2016-08-21 22:48
image: /assets/images/heroku1.png
headerImage: true
tag:
- deployment
- heroku
blog: true
author: aralyaphinith
description: deployment with Heroku
---

<div class="breaker"></div>

## Deployment with Heroku

Have a node.js (javascript) app that needs deployment?  Well Heroku is here to do just that for you, but before we get started, you will need to [create a Heroku account](https://www.heroku.com/) and then download and install the [Heroku toolbelt](https://toolbelt.heroku.com/) which will give you access to the Heroku CLI.

Once you have installed the toolbelt, open your terminal and type in 
{% highlight %}
**heroku**  
{% endhighlight %}
Dependencies for the toolbelt will begin to install.  Once that is complete, type in your terminal
{% highlight html %}
**heroku login** 
{% endhighlight %}
and enter your credentials.  Your CLI should be all set to go now.  Let's move on to your app to configure it for deployment.

Let's first configure your server file, which is usually named index.js or server.js.  The only thing that you need to have here is to set your port to **process.env.PORT**. 

<div class="environment_port">
  <img class="image" src="../assets/images/heroku2.png" alt="process.env.PORT">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

Let's look at the **package.json** file.  You will need to explicitly declare your engines here and the version of node you are using.  If you are unsure of what version of node you have, simply type in **node -v** in your terminal.  You'll also notice below that there is a start script included in this package.json file.  If you have a start script, you will not need to create a **Procfile**, but if you do not have a start script, then you will need to create a Procfile (which I will go over next).

<div class="package.json_file">
  <img class="image" src="../assets/images/heroku3.png" alt="package.json file">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

So the start script is optional, but if you do not have one in your package.json file you will need a **Procfile** in your root directory.  It must be named exactly that and in your file, you simply need the following: **web: node server.js**

<div class="procfile">
  <img class="image" src="../assets/images/heroku4.png" alt="Procfile">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

Once you have these two files setup, simply navigate to the root directory of your app and type in the terminal:
{% highlight raw %}
heroku create <name of your app>
{% endhighlight raw %}

This will create a remote to heroku's repository.  To check to see if the remote was successfully added, simply type in the command line:
{% highlight html %}
git remote -v
{% endhighlight %}

<div class="react-router">
  <img class="image" src="../assets/images/react-router4.png" alt="nav bar">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

And now finally we just need to render the routes:

<div class="react-router">
  <img class="image" src="../assets/images/react-router5.png" alt="render routes">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

For the history, you can either go with browserHistory or hashHistory.  We decided to go with hashHistory as it allowed for us to use the forward and back buttons along with the refresh button when navigating through our app (browserHistory does not allow for this).  But feel free to experiment and see what better suits your app.  The rest of the setup is pretty straighforward, assign the path name accordingly and then set your components to the name of the parent components created earlier.  Voila - you've just set up your first react-router!