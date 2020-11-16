---
layout: post
title:      "Using an arrow function vs. binding in React"
date:       2020-11-16 20:03:54 +0000
permalink:  using_an_arrow_function_vs_binding_in_react
---


Today, I was asked about the difference between an arrow function in react vs. a class function and binding it in the constructor.  To be perfectly honest, I wasn't really sure the of difference between them.  I knew both methods exsisted, but really had no solid contextual difference between the two.  

Time to study up ... 

After reading a few different articles and examples about the calling of one vs. the calling of the other and what `.bind()` is doing.  I found the following...

Let's start with `.bind()`,  this is a javascript method that allows you to send `this` as a property, so it can be utilized in the desired class function that resides in the prototype.  You are able to access `this.props` & `this.state` within the function by doing this.  Bind was the only way for your functions to access `this` up until the arrow functionality was established with ES6.

By using the `myFunction=()=>{}` your function already has access to `this` . Having that access allows for a more human readable code, and has an added bonus of being included with the component, instead of just being part of the prototype and being sent as a *callback* function.  This means less callbacks to the prototype and a faster responding application.

So the biggest questions I have after all of this are: is there some sort of safety security aspect to sending functions as a *callback* function?  Does it ultimately send more  or less information? I have yet to find an answer to these questions as of posting this.


