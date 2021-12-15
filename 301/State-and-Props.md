#Cedric's Notes for code-301n24 course

## State and Props

### React Lifecycle

- Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
Render

- What is the very first thing to happen in the lifecycle of React?
Mounting

- Put the following things in the order that they happen: 

constructor,
render,
React Updates,
componentDidMount,   
componentWillUnmount, 


- What does componentDidMount do?

This method is invoked immediately after a component is mounted. If you need to load anything using a network request or initialize the DOM, it should go here.

### Additional Resources 
React Boostrap Framework
<cite>https://react-bootstrap.github.io</cite>

Netlify to platform deploy git projects
<cite>https://www.netlify.com</cite>


### React State Vs Props

- What types of things can you pass in the props?
Arguments, can be any data type, from strings to functions, objects, etc.

- What is the big difference between props and state?
Props are passed to a component but state is handled inside of a component.
State must be updated inside the component, however props must be updated on the outside.

- When do we re-render our application?
When you change the state in your application, it will re-render that section of the application.


- What are some examples of things that we could store in state?
Props can be stored to state, 
Anything you want to re-render based off of user input.


## Things I want to know more about

Other popular react frameworks