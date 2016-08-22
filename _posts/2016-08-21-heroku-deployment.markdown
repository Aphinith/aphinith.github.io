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

Once you have installed the toolbelt, open your terminal and type in **heroku**.  Dependencies for the toolbelt will begin to install.  Once that is complete, type in your terminal **heroku login** and enter your credentials.  Your CLI should be all set to go now.  Let's move on to your app to configure it for deployment.

Let's first configure your server file, which is usually named index.js or server.js.  The only thing that you need to have here is to set your port to **process.env.PORT**. 

<div class="environment_port">
  <img class="image" src="../assets/images/heroku2.png" alt="process.env.PORT">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

Let's look at the **package.json** file.  You will need to explicitly declare your engines here and the version of the engine.  You'll also notice below that there is a start script included in this package.json file.  If you have a start script, you will not need to create a **Procfile**, but if you do not have a start script, then you will need to create one (which I will go over next).

<div class="package.json_file">
  <img class="image" src="../assets/images/heroku3.png" alt="package.json file">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

Once that is set up, then you can create your parent components as the main components to be viewed/rendered when navigating to those routes.  For this example, I have created a home page, a registration, and a profile page component.  Within each component, you can insert as many children component as you wish:

<div class="react-router">
  <img class="image" src="../assets/images/react-router3.png" alt="parent component">
  <figcaption class="caption">Photo by Aralya Phinith</figcaption>
</div>

Once those components are setup, we can create the navigation component below.  You'll notice that we use Link instead of the the href that we all are used to seing.  Also be sure to include {this.props.children} as indicated in line 59 below.  The children components within the parent component will not render without this line of code.

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