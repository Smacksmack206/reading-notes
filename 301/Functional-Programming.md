# Cedric's Notes for code-301n24 course

## Functional Programming

### Functional Programming Concepts

- What is functional programming?

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data

- What is a pure function and how do we know if something is a pure function?
It returns the same result if given the same arguments (it is also referred as deterministic)
It does not cause any observable side effects
It returns the same result if given the same arguments

- What are the benefits of a pure function?


- What is immutability?
When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

- What is Referential transparency?
Basically, if a function consistently yields the same result for the same input, it is referentially transparent.
pure functions + immutable data = referential transparency

# Videos

## Node JS Tutorial for Beginners #6 - Modules and require()

- What is a module?
We split our code in to logic modules that have certain functionality for our application

- What does the word ‘require’ do?
It passes a path to the module for the global object in node.js

- How do we bring another module into the file the we are working in?
pass a string in the require method

- What do we have to do to make a module available?
using module.exports

## Things I want to know more about

what about making a module public? 