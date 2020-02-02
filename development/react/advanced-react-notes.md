# Advanced React Notes

## React Concepts:
1. **Don't touch the DOM, I'll do it.** DOM is the Document Object Model. It's what the browser uses to display a web site or a web app and javascript is simply manipulating the DOM.
2. **Build websites like lego blocks.** The concept of reusable components. Small components that you put together to make larger components.
3. **Unidirectional data flow.** React builds using VirtualDOM which is essentially a javscript version of the DOM. and then that will send a blueprint to the DOM on how the app should look like. Data can never move up. It only moves down all the way to the DOM so if any changes happen that change the state we go back to the state and that state change trickles down to different components in one direction.
4. **I'm just the UI, the rest is up to you.** React only deals with the UI, everything else is done by using other modules and libraries to mix and match.

<br></br>
## Imperative VS Declarative: 
-**Imperative:** that is in an imperative paradigm you directly change individual parts of your app in response to various user events. so you had let's say your javascript file you'd say: hey if user is logged in.
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
- SyntheticEvent
- Prop Tunneling (Prop Drilling)
- Higer Order Component (HOC)


---

## Webpack & Babel:
 Allow us to take our source folder and **babel** is first going to make sure our javascript files are going to work on all browsers no matter what version no matter how old they are. 
 
 **Webpack** is a module bundler to let us write a modular code. Webpack will bundle all the javascript files together and optimize it for production.


 ---

## _The Job of A React Developer_
1. Decide on Components.
2. Decide the state and where it lives.
3. What changes when state changes.

---

## Sass
An upgraded version of css. It is a different language with a different file type.

create-react-app comes with configuration for sass right off the gate as long as you include it.

To include it type in your terminal: 

`npm i node-sass`

With Sass you can nest class styles inside of each other

---

## Prop Tunneling
It's a bad pattern which is basically tunneling props multiple components deep in order to get them to the component that needs them but the children in between don't actually need the props passed down for any reason other than to pass it down to its children. You never want to do this.

---

## Higher Order Component
It's essentially a function that takes a component as an argument and returns you a new modified component. Kind of like a function that gives you back a powered up component.

---

## Importing SVG in React
To import SVG in react we do it by:

`import { ReactComponent as Logo }`

This is a new special syntax when importing SVG in React. The `ReactComponent` import name is special and tells Create React App that you want a React component that renders an SVG, rather than its filename. You can read more about it here, but keep in mind that this is a React library special syntax:

https://facebook.github.io/create-react-app/docs/adding-images-fonts-and-files

---

## Redux
Redux is a library that makes state management easier it's like one massive object that describes our entire app and whichever component needs a prop can be easily passed down to it. That way none of the comopnents need to hold states anymore.

To install Redux dependencies type the following into the terminal: 

`npm install --save react-redux`


---

## Redux Concepts
- Good for managing large state.
- Useful for sharing data betweent components.
- Predictable state management using the three principles:
    - Single Source of Truth.
    - State is Read Only (Immutability => as in never gets modified but instad create a new state).
    - Changes using pure functions (recieves an input and always give back the same output every time).
- ***Reducer:*** is a pure function that recieves an input which is the action (button click) and creates an output.
- ***Store:*** That output is the store or the state which is the entire store of the app.


Note: redux basically does the same thing as this.setState