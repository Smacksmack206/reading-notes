# Cedric's Notes for code-301n24 course

## React Docs - List and Keys

What does .map() return?

A new array or list (listItems) depending on if you refering to Js or React/JSX

- If I want to loop through an array and display each value in JSX, how do I do that in React?

Using the the map() method on an array we can itirate through each element in the array and assign it to listItems and render it to the DOM by placing it in the render or using ReactDom.render.

- Each list item needs a unique "Key".

- What is the purpose of a key?
Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity

## The Spread Operator

- What is the spread operator?
it is three dots before and argument in a function call that expands an iterable object into a list of arguments.

- List 4 things that the spread operator can do.

Copying an array,
Concatenating or combining arrays,
Using Math functions,
Using an array as arguments.

- Give an example of using the spread operator to combine two arrays.

```const hello = {hello: "123"}```
```const world = {world: "456!"}```
```const helloWorld = {...hello,...world}```

- Give an example of using the spread operator to add a new item to an array.

```const myArray = [`a`,`b`,`c`]```
```const yourArray = [`d`,`e`,`f`]```
```const ourArray = [...myArray,...yourArray]```

- Give an example of using the spread operator to combine two objects into one.
```const objectOne = {hello: "ab"}```
```const objectTwo = {world: "cd"}```
```const objectThree = {...objectOne, ...objectTwo, cash: "money"}```

## Video - How to Pass Functions Between Components

- In the video, what is the first step that the developer does to pass functions between components?
Create the function wherever the state is that you want to change

- In your own words, what does the increment function do?
uses the people objects that is in state and updates the count if it matches a name and returns the updated people objects and places it in the ppl variable as a new array

- How can you pass a method from a parent component into a child component?
Pass it as a prop using this. on the method you are passing

- How does the child component invoke a method that was passed to it from a parent component?
this.props. on the method you passed to the child with parentheses following. 

## Things I want to know more about

A better understanding of how React compiling process.