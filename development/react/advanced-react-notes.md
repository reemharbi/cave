# Advanced React Notes

## React Concepts:
- **Don't touch the DOM, I'll do it.** DOM is the Document Object Model. It's what the browser uses to display a web site or a web app and javascript is simply manipulating the DOM.
- **Build websites like lego blocks.** The concept of reusable components. Small components that you put together to make larger components.
- **Unidirectional data flow.** React builds using VirtualDOM which is essentially a javscript version of the DOM. and then that will send a blueprint to the DOM on how the app should look like. Data can never move up. It only moves down all the way to the DOM so if any changes happen that change the state we go back to the state and that state change trickles down to different components in one direction.
- **I'm just the UI, the rest is up to you.** React only deals with the UI, everything else is done by using other modules and libraries to mix and match.

<br></br>
## Imperative VS Declarative: 
**Imperative:** that is in an imperative paradigm you directly change individual parts of your app in response to various user events. so you had let's say your javascript file you'd say: hey if user is logged in.
Well then go change that little icon over here to the user's profile. And now that the user is logged in, well, also show profile page.

OK so javascript goes changes the Dom and updates the profile page and then OK.

Now that we have we're also logged in.

We also need to display friends.

OK.

This sounds intuitive but the problem with this imperative approach is that it becomes difficult to see the relationships between events and all these edge cases.

---

**Declarative:** The declarative paradigm is called that because we declare that hey this is what the state or data of our app should be like. And based on this date. Well then just make those changes. 

So if a user is logged in then React already knows exactly what to update and what to do. 

Now this idea of a declarative style meant that we didn't have to directly say do this and if this happens then do that where we just say one by one exactly what should happen. Instead we tell it this is the state of our app and React automatically just does it for us.


<br></br>
## React Keywords:
- Declarative
- JSX
- State
- Props
- Components
- VirtualDOM


