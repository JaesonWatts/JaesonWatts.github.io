---
layout: post
title:      "mapBrainToBlog"
date:       2020-09-23 17:01:06 +0000
permalink:  mapbraintoblog
---


You’re learning React / Redux, and you just learned about mapStateToProps() and mapDispatchToProps() and now you think you might have an aneurysm because WHOA WHAT???
I know the feeling and I’m here to “connect()()” the dots!

When you have an application built with react /redux you have access to this thing called the Global Store, and that store has a “state”, which is literally just that, it’s current state.  We can’t change the state directly, we can only make a new state and replace the old one, filing it away like an old lithograph, a static slice of the past. But the important thing about this is how we access this state in our applications and how the state becomes a property.

First we need to look at the connect()() function to understand mapStateToPRops and mapDispatchToProps.  Connect is what allows us to access state and make it useful.
Here is the relevant syntax:

<code>
export default connect(mapStateToProps, mapDispatchToProps)(component or container receiving props)
</code>

The truth is we are writing these functions because if we didn’t our application wouldn’t know what parts of the state we wanted to map to our props! In our code below we are saying to our mapStateToProps function “here is the whole state, please take the personas from the state and return that as a prop called ‘personas’ k thnx!”

<code>
const mapStateToProps = state => {
  return {
    personas: state.personas
  }
}
</code>
 


And that is just what it does! And in the last set of parentheses in our connect function we define the component or container that is going to receive the props, so if we wanted to be available as a prop for the App component we would just ..

<code>
export default connect(mapStateToProps, mapDispatchToProps)(App)
</code>


.. and bip, we are connected!

But wait Jaeson! What about mapDispatchToProps? Where does that come in? Let’s take a look.

<code>
export default connect(mapStateToProps, {fetchPersonas})(PersonasContainer)
</code>

Hey, wait a second! That doesn’t look like mapDispatchToProps! That says fetchPersonas!
Yes. So when you have an action in React you need to dispatch that action to a reducer, where logic is implemented and something is returned. In order to have access to that return in your props in your container or component you need a method to take that dispatch return and, well, map it to props, just like we did before.  Now we could write the mapDispatchToProps like this:
<code>
const mapDispatchToProps = dispatch => {
  return {
    personas: () => {
      dispatch(fetchPersonas())
    }
  };
};
</code>

What this would do is set the prop ‘personas’ equal to the return of the dispatch function with the action creator fetchPersonas passed in, “wrapped in dispatch” you could say. So to make our code a little cleaner we abstract the idea of mapDispatchToProps as inherent to the second argument in our connect function. 

I hope this little blog has helped clarify your understanding of how connect()() uses mapStateToProps and mapDispatchToProps to make state and your dispatched action returns available as props in your application.

Stay safe and keep coding!



