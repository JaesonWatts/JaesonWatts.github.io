---
layout: post
title:      "Routes and Relationships 2: Nested Routes, Nested Headaches"
date:       2020-07-20 16:54:54 -0400
permalink:  routes_and_relationships_2_nested_routes_nested_headaches
---




It's crunch time. Your nested routes aren't nesting. And unlike a pregnant kitty our nesting isn't an instinctual, natural occurrence.

Why is nested routing even important Jae? I can hear you asking this wonderful question.
Well to explain that we need to talk about what routes and resources are.

A route is our code that  provides us with the paths to our view and actions.  Routes are found in config/routes.rb and are arguably some of the most important code in our project, though it's truly hard to quantify that. However in the author’s opinion a view or action are worthless if you don’t know how to get there! Buying a new house is only helpful if we know how to show up and move in!  Our controllers are the instructions on how to move in but those won’t work if we are at the wrong house. 
<img src="https://i.imgur.com/bLKUKwN.png" alt="routes.rb" width="70%">

When we have models that are natural children of another model it works well for our purposes to have a route that shows that parent-child relationship. /den/1 is ok but /pack/1/den/1 tells me a whole lot about the origin of that pack.  Our ActiveRecord relationships allow us to do some cool things like @pack.dens, or @den.pack, or even @den.scouts.  Our nested routes allow us to display relationships like that on the url.
<img src="https://i.imgur.com/OSAC2lx.png" alt="routes.rb" width="70%">

But wait there’s more!  What if I told you that when we make new instances of a model this nested relationship allows us to define that relationship right there in the form?  Well buckle up because I’m about to! 

When we have our forms call upon that nested route it allows us to use neat little helpers like collection_select, which will give us a dropdown menu of all the parent instances, and collections_check_boxes, which gives us relational options similar to the previous helper but with check boxes instead. This allows us to create the parent-child relationship with ease in the creation phase. Making things easier is what all this coding is all about after all, isn’t it?
<img src="https://imgur.com/2N9HOTP" alt="routes.rb" width="70%">



Nested resources secret power is in the passing of params from place to place. Specifically the :parent_id in the case of my app, the Cub Scout Manager, which is the param I need to keep around as we go from view to view, through our routes and controllers, in order to maintain that relationship from the showing of our instance to creating a new one.

The real key in the end is to not get hung up on how complicated it looks, but to start trying it out in your code, breaking things and fixing them, until you have the results you want. In the end you will find out that it’s a bit simpler under the hood.

Before I leave I want to drop one more bit of knowledge your way.  My favorite way of debugging is to drop in my code this little ditty:


<%raise params.inspect%>

It is very much like a binding.pry or a byebug in that it creates a terminal instance, but in this case it creates it right in the browser view along with a whole lot of useful debugging information for you to use. When you are done, delete the code, refresh the page, and carry on with your day, richer for the knowledge!  There are other things you can raise, I challenge you to stretch and investigate the other raises one can make. 

That’s all for now!
Stay safe and keep coding!

