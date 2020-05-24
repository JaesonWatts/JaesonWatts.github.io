---
layout: post
title:      "Hashes of an array instead of an array of hashes "
date:       2020-05-24 02:55:20 +0000
permalink:  hashes_of_an_array_instead_of_an_array_of_hashes
---


I promise you it’s not a tongue twister. In my Cli project I chose to create a global variable to hold the parsed output from our Api call and to only store the systems I chose to save into the @@all array and they weren’t actual instances of a System as created by System.new.  While it worked for the purposes of the application I learned in my project review that it most definitely was not the best way to approach things.  
During the review we refactored to truly utilize the class with System.new and then assigned the system attributes from the parsed api return as attributes for the System instances, making the @@all array truly “all” of the systems. Now we have a new class array called @@saved that will hold the systems we chose to save.

![](https://i.imgur.com/NugXjoO.png)

Doing things this way allows us a whole new layer of flexibility when it comes to working with our system data.  Previously we had one Ruby object, a global variable, that was our whole set of data we got back from the api. Now we have a Ruby object that represents each different system, which more accurately represents in code the real life objects we are trying to search through. This allows us to have a more intuitive and flexible interaction with our data, improving readability and our future additions to the operations we want to perform on our data, such as fuel calculations.  Calculating distance between two separate objects seems like it is inherently more manageable as opposed to trying to run those same calcs within the object space of a singular variable, no matter how many items it contains as an array, especially once your searches take you into results with hundreds of systems.
