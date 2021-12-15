#Cedric's Notes for code-201n24 course

# <cite> Reading from the Jon Duckett JavaScript book </cite>

## Error Handling & Debugging

### Order of execution (pp.452)
- Explains how scripts are processed

### Understanding Errors (pp.458)
- If there is an error the interpreter will look for exception handling code all through the stack until it reaches the end and throws an error object.

### Error Objects (pp.459)
Explains how error objects can help you fix your code with tools browsers provide also explains what the errors mean.

### Inspect with different browers(pp.464-470)
Covers various browsers and tools for inspecting and debugging code.

### Handling Exceptions (pp.480)
If you know your code might fail, use ( try, catch, and finally.)

Each is given its own code block.

Try
You specify the code you think might throw an error within thje try block.

Catch
If the try code throws an exepction, catch ssteps in with an alternative code set.

Finally
The contents of the code will run either way - wether try block successed or not.

``` try {
    
} catch (execption) {

} finally {

}  ```