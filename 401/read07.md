# Global Variables
---
### In Python, a variable declared outside of the function or in global scope is known as a global variable. This means that a global variable can be accessed inside or outside of the function.

### Let's see an example of how a global variable is created in Python.

## Example 1: Create a Global Variable
---
#### x = "global"

#### def foo():
####     print("x inside:", x)


#### foo()
#### print("x outside:", x)
---
## Output :

#### x inside: global
#### x outside: global
--- 

### In the above code, we created x as a global variable and defined a foo() to print the global variable x. Finally, we call the foo() which will print the value of x.

#### What if you want to change the value of x inside a function?
---
#### x = "global"

#### def foo():
####    x = x * 2
####    print(x)

#### foo()
## Output :

### UnboundLocalError: local variable 'x' referenced before assignment

---

### The output shows an error because Python treats x as a local variable and x is also not defined inside foo().

---

# Nonlocal Variables

### Nonlocal variables are used in nested functions whose local scope is not defined. This means that the variable can be neither in the local nor the global scope.

### Let's see an example of how a nonlocal variable is used in Python.

### We use nonlocal keywords to create nonlocal variables.

## Example : Create a nonlocal variable

#### def outer():
####    x = "local"

####    def inner():
####        nonlocal x
####       x = "nonlocal"
####        print("inner:", x)

####    inner()
####    print("outer:", x)


#### outer()
---
## Output

#### inner: nonlocal
#### outer: nonlocal
---

# What is Big O Notation?
#### Big O notation is used in computer science to describe the performance or complexity of an algorithm. Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used by an algorithm. It is hard to pin down the exact runtime required by an algorithm, it depends on what processor you use, what other programs the computer is running. So instead of calculating that, we use a concept to see how quickly the runtime grows. Imagine when we write a piece of code, we would more likely end up in refactoring it not just because we want to keep the application DRY, but we want to make sure the efficiency of our code, which is directly related to user experience.
---

### Making Sense of Big O Notation
#### Before any example, here are some concepts you need to know first:
#### 1) Size of input: we call it “n”. So we can say things like, we have a function which takes a parameter of an array of integers. Then the input here refers to the array.
#### 2) The rules: In big O analysis, it only cares about the code that grows the fastest as the input grows, because everything else eclipsed(big O analysis is also called asymptotic analysis).

![](https://miro.medium.com/max/1400/1*Uzrw9faXdYgg20I6NjUTBw.png)


---
### references :
---
[medium](https://medium.com)
[tutorialspoint](https://www.tutorialspoint.com)
