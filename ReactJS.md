[React-LifeCycle]: img/low-level-lifecycle.png
[Flux-Cycle]: img/flux.png

# ReactJS Study Guide

# 1. What is ReactJS?

React is a UI library developed by Facebook. Facebook uses in production and instargram is built entirely with React.

React uses the Virtual DOM that selectively renders subtress of nodes base upon state changes. It does least amount of DOM manipulation in order to keep components up to date. 

# 1a. How does React work?
When there is a change in the state. 

 1. React uses a "diffing" algorithm
 2. Reconciliation, where it updates the DOM with the results of the difference.

Rather than starting over with a clean state it actually only changes the components where the slice of state is changed.

# 2. What happens during the lifecycle of a React Component?

At a high-level it is broken into 3 parts:  
1. Initialization
2. State/Property Updates
3. Destruction

Low-level:

![Low-Level Life Cycle][React-LifeCycle]


# 3. What can you tell me about JSX?

When Facebook introduce ReactJS to the world they also create a dialect JSX which allows embeded raw HTML to their JavaScript. Browsers can't render direct JSX which needed babel and webpack to convert JSX to JS. JSX has been the de facto of creating React Components.

Developing with JSX allows a declarative syntax which reduces the complexity of the code. Developing with JSX developers with adopt ES2015 syntatic sugar: class, block scoping, and the new spread operator.

Examples of experiences:
```
    It took a bit of time at first getting use to JSX and ES2015 but after learning it, I discoverd how much I enjoy JSX and ES6. Specifically, I am a big fan of Class syntax ES6 has to offer which is closer to lower-level languages like Java which makes the code declarative and reduces the amount of overhead. The code becomes more readable with less overhead.

    But on the other hand I can do without configuring webpack but it is a necessary evil to improve quick deployment and creating components quickly.
```

# 4. Are you familiar with Flux?

Flux is an architectural pattern that forces unidirectional data flow. Flux design patttern is generic, so you can apply these concepts outside of React Applications.

![Flux Cycle][Flux-Cycle]

- Action
    - The only way to for view components to trigger changes to the store. The send a mandatory type key and optional payload keys containing new information. They are sent using the store.dispatch() and are the primary drivers of Redux loop.
- Dispatcher
    - Dispatches actions.
- Store
    - Holds the global state of an application. Central component of the Redux's architecture.
    - Updates App state with the reducers.
    - Listens for actions to change the global state.
- Reducer
    - Updates the store's state.
    - Receives the current state and action
    - Updates the state appropriately based on the action.type
    - returns the next state
    - You should never mutate its arguments(i.e. state and action). Returns a new object if state changes.
        - Use ``` Object.freeze(state); ```
- View
    - 


A popular library which implements flux in react is Redux.
``

# 5. What are stateless components?
They are reusable components also known as pure functions. Renders onto the DOM, solely with properties that provided. 


# 6. What is Middleware?
# 6a. Explain

# 7. How does ReactJS work?
