
# Error
---

#### Error objects are thrown when runtime errors occur. The Error object can also be used as a base object for user-defined exceptions.

# Error types

#### Besides the generic Error constructor, there are other core error constructors in JavaScript. For client-side exceptions, see Exception handling statements.

## EvalError
#### Creates an instance representing an error that occurs regarding the global function eval().
## RangeError
#### Creates an instance representing an error that occurs when a numeric variable or parameter is outside of its valid range.
## ReferenceError
#### Creates an instance representing an error that occurs when de-referencing an invalid reference.
## SyntaxError
#### Creates an instance representing a syntax error.
## TypeError
#### Creates an instance representing an error that occurs when a variable or parameter is not of a valid type.
## URIError
#### Creates an instance representing an error that occurs when encodeURI() or decodeURI() are passed invalid parameters.
#### AggregateError
#### Creates an instance representing several errors wrapped in a single error when multiple errors need to be reported by an operation, for example by Promise.any().
## InternalError 
#### Creates an instance representing an error that occurs when an internal error in the JavaScript engine is thrown.

![](https://www.tutsmake.com/wp-content/uploads/2020/05/Types-of-Errors-In-JavaScript.jpeg)


#  handling 
---

#### we have several way to handling the errors

![](https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/08/JavaScript-Errors-1200x720.jpg)

## Throwing a generic error
#### Usually you create an Error object with the intention of raising it using the throw keyword. You can handle the error using the try...catch construct:


![](https://miro.medium.com/max/5488/1*xCKNCE7ymRy5pAcmfBiPDw.png)


## Handling a specific error
#### You can choose to handle only specific error types by testing the error type with the error's constructor property or, if you're writing for modern JavaScript engines, instanceof keyword:
---
#### try {
####  foo.bar()
#### } catch (e) {
####   if (e instanceof EvalError) {
####     console.error(e.name + ': ' + e.message)
####   } else if (e instanceof RangeError) {
####     console.error(e.name + ': ' + e.message)
####  }
  
#### }
---

## References:
---

[mozilla](https://developer.mozilla.org/)
[w3schools](https://www.w3schools.com/)
