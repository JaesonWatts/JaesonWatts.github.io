---
layout: post
title:      "The Digital Diner"
date:       2020-09-21 03:59:56 -0400
permalink:  the_digital_diner
---


Imagine, if you will, a diner. Not Just any diner, it’s the digital diner and they are serving up pie on special.  Today I will use the analogy of this diner to explain to you how javascript promises, react, and redux all work together to serve your pie, aka your data, to you.

First we need to cover some basics.  This blog will assume that you have at least a basic understanding of what javascript is.

You are hungry, so you decide to head to the diner to get some food. You roll up,head inside, and get seated by the waitress. After time to look at the menu she comes and takes your order on her ticket, which she then takes to the counter where she hangs it and the cook makes it and sends it back. You might not realize it yet but this is the same flow as a react-redux application. 

![](https://i.imgur.com/eklPPo0.png)



Allow me to explain.

In our application we have several different pieces that all fit together to make our whole.
The store, provided by redux, is where we store our data.  We have our action creators which we then send our actions through our reducers, where the action is completed, and then the results are dispatched back to the store, and then to us, the user.

Let’s connect the dots shall we?

The diner represents our application, and we are, well, us, the user. We go inside, aka open the application, and create our actions. 


“I would like the breakfast special plate” we say, as the waitress scribbles on her pad.  She’s the reducer, here to turn our created action, BUY_SPECIAL, into reality for us.  
![](https://i.imgur.com/o2InGFS.png)


She took our order and left us with a coaster and a cup of water and placed the ticket on the order window of the kitchen. The kitchen in our backend api, the order window counter is our store. 

![](https://i.imgur.com/puLr5Uw.png)


 The coaster and water on our table is the promise on the front end “I have your order, and as soon as it’s ready I will bring it to you!” and the ticket is the fetch request “hey can I have this food?” which in our application is our data, right, because we are consuming it.  
 
 ![](https://i.imgur.com/CjqnkCq.png)

Soon our food is done, the cook has put the plate on the order window counter(the api has returned our data to the store) and we are ready to have that food delivered to our table (data dispatched to our User Interface).  

![](https://i.imgur.com/SLwdiM9.png)

The waitress comes back over and serves it up to us at the table(renders the data from the store into the dom).
What a meal, eh? 
I hope this little story about a tiny diner has helped you understand a little bit more about how React, Redux, and JavaScript asynchronous promises work together to create a full featured application.

