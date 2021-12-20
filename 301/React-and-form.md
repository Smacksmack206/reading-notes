# Cedric's Notes for code-301n24 course

## React Docs - Forms

- What is a ‘Controlled Component’?
a component renders form elements and controls them by keeping the form data in the component's state.

- Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
Use onChange event handler to update state as they type, so that when they submit the state will have all of the input data.

- How do we target what the user is entering if we have an event handler on an input field?
event.target.value

## The Conditional (Ternary) Operator Explained

- Why would we use a ternary operator?
Shorten if statements lines of code

- Rewrite the following statement using a ternary statement:

``` javascript
if(x===y){ console.log(true);
} else {
 console.log(false);
  } 
```

``` x===y ? 'console.log(true)' : 'console.log(false)'; ```

## Things I want to know more about

curious to see examples of passing data with multiple forms between multiple componnets.
