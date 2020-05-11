---
layout: post
title:      "My CLI Project"
date:       2020-05-11 07:42:57 +0000
permalink:  my_cli_project
---


For my CLI project I decided to use an API to fetch some data.  Conveniently I was talking with a friend of mine about our desire for our own personal Star Finder and Course Plotter for Elite Dangerous, a game we have played together for years, and while this project comes nowhere close to the scope of our discussed plans, the framework is laid down in this project for expansion into the sweet info machine we envision.

This being my first piece of real working software I went into this somewhat intimidated, but once I started diving into the code I was able to keep it in perspective and stopped being overwhelmed.  I was reminded by my cohort lead to “just worry about making it work first” so that is just what I did.  

The first working draft was rather ugly, all the code smashed into two files.  Once I got everything displaying properly I spent a TON of time both in the terminal and in binding.pry trying to figure out how best to make use of the API. Once I had everything working it was time to refactor and bring a little more structure to the project. 

I had a handful of things in mind for making this a well written project. The first thing was the following: 
    “If I find myself writing the same code a second time it’s time to stop and write a method for it.”

It helped immensely, as I usually found anything written twice was written again!  Eventually with that mindframe I was able to anticipate those moments and would write the method name for methods I haven’t written yet, counting on the errors at run time to help me remember to write them.

The second was a general idea of how I wanted the file structure for the menus to work, with the idea that I would revisit this project and want to expand.  The problem with expansion is that bloated code can be hard to add new features to once you hit a certain size. It’s tiny now but it won’t always be if we keep adding to it!  To combat expansion bloat I organized the menu folders in handlers and displayers. Organized in this way I can track down the code for a menu option to change it or debug it.

There were a few challenges in this project that I really enjoyed, and I look forward to continuing to work on this gem and grow it towards the full service system finder I envision.

