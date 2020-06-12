---
layout: post
title:      "Routes and relationships"
date:       2020-06-12 10:12:49 +0000
permalink:  routes_and_relationships
---


For my second project I again chose something video game related, a member management system and ultimately a computer aided dispatch for an online modding and roleplay community.  If I were to be asked to pick the hardest thing for me to grasp and put into practice in this project I would be hard pressed to do just that, pick one. The dynamic duo in this little brain stretching party were Restful Routes and ActiveRecord::Relationships (see what I did there?)

First let's talk about relationships, because in truth, it all starts there.  I began my design of this project with a hand drawn set of tables, with the idea being that if I know what the tables are and how they relate then everything else should fall into place. Things fell alright, but I’m not sure into place was where it was falling at first!
<img src="https://i.imgur.com/fHL46no.jpg" width="70%">

By having my tables clearly laid out and was able to build the structure of the program very methodically, writing the migrations that will build our virtual representation of that thing on the paper, that itself was a model of some other, non physical model of some other thing in real life. If that isn’t a deep meta for the dynamic and abstract world of software engineering I don’t know what is!! From there it was a cinch to create the model, view, and controller for each table.  This is where the relationships come in, and I’m again saved by my primitive scribblings on tree pulp. Sort of. 

<img src="https://i.imgur.com/hC1U5On.jpg" width="70%">

Creating the “has_many, has_one, has_this_many through: :the_thing” looked daunting at first , a complicated mess more sticky than 16 years of marriage was!  But a few sessions of washing dishes while refreshing on the topic, then reading the lesson again, I was able to make some sense of the whole spaghetti mess. Let’s just say a LOT of dishes were done before I “grokked” it but when I did suddenly I was breezing through binding.pry consoles like a surfer on a wave, grabbing persona.member and member.guns and other fun and related data grabs. It’s all about the data, and how you need to access it. 
But then it was time to make the routes. Aahh the routes. I was not friends with the routes at first. Routing requests through a single controller wasn’t that complicated but I decided to be fancy and bite off a big bite of the sandwich and had millions of controllers!

<img src="https://i.imgur.com/Yl2ahuA.jpg" width="70%">

 Well, ok, not millions, but when I was staring at the screen we all love so much, you know the one, it started to feel like millions as I stumbled trying to figure out why "wHY oGM WHY WONT YOU ROUTE!!??"  I got past that eventually, my dev buddies laughing on the other side of a voice chat at my frustrated tone.
 
<img src="https://i.imgur.com/7LBR55r.png" width="70%">

The key for me was, as usual, a liberal sprinkling of binding.pry, and that sweet feature of vscode where I can have a four or five different files open on the screen like tiles, as I do my best impression of Sherlock Holmes and the mystery of the extra “/”, a stumbling Watson waiting for those flashes of brilliance as I weave my way across views and controllers binding the broken links together to tell the story I want to tell with my “restful” api.  

In the end this was a difficult project for me, as grasping these two concepts well enough to put them into practice was not an easy process for me. I could make excuses about the times but we aren't here for that, suffice to say that despite the difficulties I had, I DID grasp these concepts and have the satisfaction of seeing my creation come to life, something I will be adding to and utilizing myself as time goes on.  

Thanks for reading, stay safe, and keep coding!


