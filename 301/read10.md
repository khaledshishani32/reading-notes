# In memory storage

---

### 1) What is a ‘call’?
- is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.

### 2) How many ‘calls’ can happen at once?
-  one at a time, from top to bottom. It means the call stack is synchronous.

### 3) What does LIFO mean?
- Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).



    
 
### 4) What causes a Stack Overflow?
- when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.





--- 
### 1) What is a ‘refrence error’?

-  The ReferenceError object represents an error when a non-existent variable is referenced.




### 2) What is a ‘syntax error’?
- Syntax errors are detected while compiling or parsing source code. For example, if you leave off a closing brace ( } ) when defining a JavaScript function, you trigger a syntax error.
 

 
### 3) What is a ‘range error’?
- A RangeError is thrown when trying to pass a value as an argument to a function that does not allow a range that includes the value. 

### 4) What is a type error’?

- The TypeError object represents an error when an operation could not be performed, typically (but not exclusively) when a value is not of the expected type.

### 5) What is a breakpoint?
- At each breakpoint, JavaScript will stop executing, and let you examine JavaScript values. After examining values, you can resume the execution of code (typically with a play button).
- 


### 6) What does the word ‘debugger’ do in your code?
- The debugger keyword stops the execution of JavaScript, and calls (if available) the debugging function. This has the same function as setting a breakpoint in the debugger. If no debugging is available, the debugger statement has no effect.
---
### references :
---
[nodejs](https://nodejs.dev/learn)
[stackoverflow.](https://stackoverflow.com)
[educative](https://www.educative.io)
[flow.org](https://flow.org/en/docs/react/components/)