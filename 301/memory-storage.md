# Cedric's Notes for code-301n24 course

## In memory storage

### Understanding the JavaScript Call Stack

- What is a ‘call’?
The call stack is primarily used for function invocation (call).

- How many ‘calls’ can happen at once?
 Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.

- What does LIFO mean?
Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

- Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.


- What causes a Stack Overflow?
A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

### JavaScript error messages

- What is a ‘Reference error’?
This is as simple as when you try to use a variable that is not yet declared you get this type os errors.


- What is a ‘syntax error’?
I know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

- What is a ‘range error’?
Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

- What is a Type error’?
Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

- What is a breakpoint?
Conditional to stop program when condition is met

- What does the word ‘debugger’ do in your code?
Cause a breakpoint in the line you want to break

## Things I want to know more about

N/a