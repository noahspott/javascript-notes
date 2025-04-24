# Course Notes - The Hard Parts of Async JS

## Introduction

### What are the two parts of an **execution context**?

1. **Thread of execution** - the order in which statements and expressions are executed
2. **Variable environment** - the collection of variable names

### What's the difference between parameter and argument?

**Parameter** - the variable in the function definition
**Argument** - the actual data passed to the function

## Asynchronous JavaScript

### How many threads does JS have?

Just 1!

### What are some examples of Web Browser API's?

- console
- setTimeout
- localStorage

### What actually handles setTimeout?

The browser

### What is the feature in the browser that handles setTimeout?

Timer

### Is setTimeout a JS function?

Not in how you might think.

It's a facade function, meaning it doesn't actually handle the functionality of the setTimeout function.

It tells the browser to handle it.

### Is setTimeout(()=> console.log("Hello"), 1000) guaranteed to run after 1s?

No.

It's possible that there is other synchronous code that takes longer than 1s to run, like an infinite loop.
