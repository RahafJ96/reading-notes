# JS Debugging
When executing JavaScript code, different errors can occur.
Errors can be coding errors made by the programmer, errors due to wrong input, and other unforeseeable things.When programming code contains errors, nothing will happen. There are no error messages, and you will get no indications where to search for errors.

Searching for (and fixing) errors in programming code is called code debugging.

1. The console.log() Method
If your browser supports debugging, you can use `console.log()` to display JavaScript values in the debugger window

2. Setting Breakpoints
At each `breakpoint`, JavaScript will stop executing, and let you examine JavaScript values.

3. The debugger Keyword
The `debugger` keyword stops the execution of JavaScript, and calls (if available) the debugging function.

## JavaScript try and catch
- The `try` statement allows you to define a block of code to be tested for errors while it is being executed.

- The `catch` statement allows you to define a block of code to be executed, if an error occurs in the try block.

**The JavaScript statements try and catch come in pairs:**
```javascript
try {
  //Block of code to try
}
catch(err) {
  //Block of code to handle errors
}
```

Or you can use these statements to catch the error:

- The `throw` statement lets you create custom errors.
```javascript
throw "Too big";    // throw a text
throw 800;          // throw a number
```

- The `finally` statement lets you execute code, after try and catch, regardless of the result.
```javascript
try {
  //Block of code to try
}
catch(err) {
  //Block of code to handle errors
}
finally {
  //Block of code to be executed regardless of the try / catch result
}
```

## Object Errors:
There are three types of errors in programming:

### 1.Syntax Errors
Syntax errors, also called parsing errors, occur at compile time in traditional programming languages and at interpret time in JavaScript.

For example, the following line causes a syntax error because it is missing a closing parenthesis.

```javascript
<script type = "text/javascript">
      window.print(;
   
</script>

```

### 2. Runtime Errors
Runtime errors, also called exceptions, occur during execution (after compilation/interpretation). For example, the following line causes a runtime error because here the syntax is correct, but at runtime, it is trying to call a method that does not exist.

```javascript
<script type = "text/javascript">
      window.printem(;
   
</script>

```
### 3. Logical Errors
Logic errors can be the most difficult type of errors to track down. These errors are not the result of a syntax or runtime error. Instead, they occur when you make a mistake in the logic that drives your script and you do not get the result you expected.

## The onerror() Method
The `onerror event` handler was the first feature to facilitate error handling in JavaScript. The error event is fired on the window object whenever an exception occurs on the page.


The onerror event handler provides three pieces of information to identify the exact nature of the error −

- `Error message` − The same message that the browser would display for the given error

- `URL` − The file in which the error occurred

- `Line number` − The line number in the given URL that caused the error

You can use onerror with many HTML tags to display appropriate messages in case of errors. such as image:
```javascript
<img src="myimage.gif" onerror="alert('An error occurred loading the image.')" />
```