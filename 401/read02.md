# Testing and Modules

---

### Today Continuous Integration and Continuous Deployment(CICD) is an integral part of software development and deployment. To implement CICD for Data Science projects we first need to adopt Test Driven Development(TDD). In this blog, we will learn why do we need TDD, what is TDD, how does it work and finally implementation in Python using fixtures

## What is Test Driven Development?
### TDD is the process of building tests cases for all the use cases or scenarios we will code for. We will run these tests every time we compile our code.
### TDD approach of writing a failed unit test cases, then writing the production code to make it pass and then refactoring the code provides an immediate feedback on the code.

## Benefits of TDD
### Awesome test coverage : We first write the test case first that way we never miss to include test case for the conditions written in the production code. This gives our production code a very high test coverage almost 90% to 100%. This makes our code bug free.
### Immediate Feedback : Making changes to previously written production code that has the potential to break the production code is easily eliminated by TDD as the test cases would break.
### Clean and Simple : As we build small chunks of code step by step. This help keep our code simple and manageable. Also we document the code as we build the code
---
## If name equals main

### ‘__main__‘ is the name of the scope in which top-level code executes. A module’s __name__ is set equal to ‘__main__‘ when read from standard input, a script, or from an interactive prompt.

### It means that if any module/python file is running as the main program, it sets the special__name__ variable to have a value ‘__main__‘



---

## Recursion in Python


### A function that calls itself is a recursive function. This method is used when a certain problem is defined in terms of itself. Although this involves iteration, using an iterative approach to solve such a problem can be tedious. The recursive approach provides a very concise solution to a seemingly complex problem. It looks glamorous but can be difficult to comprehend!

### The most popular example of recursion is the calculation of the factorial. Mathematically the factorial is defined as: n! = n * (n-1)!

### We use the factorial itself to define the factorial. Hence, this is a suitable case to write a recursive function. Let us expand the above definition for the calculation of the factorial value of 5.:

### 5! = 5 X 4!
###      5 X4 X 3!
###      5 X4 X 3 X 2!
###      5 X4 X 3 X  2 X 1!
###      5 X4 X 3 X  2 X 1
###    = 120

 










---
### references :
---
[Tutorialsteache](https://www.tutorialsteacher.com)
[Google](https://www.google.com)
