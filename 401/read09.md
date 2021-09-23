## What is functional programming?
Is a programming paradigm **— a style of building the structure and elements of computer programs —** that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.

## What is a pure function and how do we know if something is a pure function?
To know if a function is pure or not according to the following:
1. t returns the same result if given the same arguments.
2. It does not cause any observable side effects.

## What are the benefits of a pure function?
1. The code's definitely easier to test. We don't need to mock anything.
2. Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result.

## What is immutability?
When data is immutable, its state cannot change after it's created. If you want to change an immutable object, you can't. Instead, you create a new object with the new value.

## What is Referential transparency?
It assures you the purest function will always have the same output, given the same input.Basically, if a function consistently yields the same result for the same input, it is referentially transparent.

# Node js Modules and Require:
## What is a module?
It is another javascript file that is used to organize our work rather than putting all in a single file that is the App.js because if we keep it in the App.js it will become very messy.

## What does the word `'require'` do?
Is a built-in function to include external modules that exist in separate files. `require()` statement basically reads a JavaScript file, executes it, and then proceeds to return the export object.

## How do we bring another module into the file the we are working in?
We use export by the syntax: module.export = the name of the class.