# Cedric's Notes for code-301n24 course

## Putting it all together

### React Docs - Thinking in React

1. What is the single responsibility principle and how does it apply to components?
Componnets, functions, and objects should all follow the single responsibility principle which is any of the above should only do one thing.

2. What does it mean to build a ‘static’ version of your application?
No interactivity.

3. Once you have a static application, what do you need to add?
Figure out the absolute minimal representation of state your application needs to compute

4. What are the three questions you can ask to determine if something is state?
- Is it passed in from a parent via props? If so, it probably isn’t state.
- Does it remain unchanged over time? If so, it probably isn’t state.
- Can you compute it based on any other state or props in your component? If so, it isn’t state.

5. How can you identify where state needs to live?
- Identify every component that renders something based on that state.
- Find a common owner component (a single component above all the components that need the state in the hierarchy).
- Either the common owner or another component higher up in the hierarchy should own the state.
- If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.

### Higher-Order Functions

1. What is a “higher-order function”?
Functions that operate on other functions, either taking them as arguments or by returning them, are called higher-order-functions.

2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?
returning a arrow function comparing the M parameter vs a value it takes as a argument with N

3. Explain how either map or reduce operates, with regards to higher-order functions.
taking in function values from other functions combining array value sums.

## Things I want to know more about
No questions come to mind at this time.