# Classes and Objects

---

### A class is a user-defined blueprint or prototype from which objects are created. Classes provide a means of bundling data and functionality together. Creating a new class creates a new type of object, allowing new instances of that type to be made. Each class instance can have attributes attached to it for maintaining its state. Class instances can also have methods (defined by their class) for modifying their state.

### To understand the need for creating a class let’s consider an example, let’s say you wanted to track the number of dogs that may have different attributes like breed, age. If a list is used, the first element could be the dog’s breed while the second element could represent its age. Let’s suppose there are 100 different dogs, then how would you know which element is supposed to be which? What if you wanted to add other properties to these dogs? This lacks organization and it’s the exact need for classes. 

### Class creates a user-defined data structure, which holds its own data members and member functions, which can be accessed and used by creating an instance of that class. A class is like a blueprint for an object.

### Some points on Python class:  

- Classes are created by keyword class.
- Attributes are the variables that belong to a class.
- Attributes are always public and can be accessed using the dot (.) operator. Eg.: Myclass.Myattribute

## Class Definition Syntax:

#### class ClassName:
####  # Statement-1
    .
    .
    .
####     # Statement-N
---
# Class Objects
### An Object is an instance of a Class. A class is like a blueprint while an instance is a copy of the class with actual values. It’s not an idea anymore, it’s an actual dog, like a dog of breed pug who’s seven years old. You can have many dogs to create many different instances, but without the class as a guide, you would be lost, not knowing what information is required.


### An object consists of : 

#### State: It is represented by the attributes of an object. It also reflects the properties of an object.
####  Behavior: It is represented by the methods of an object. It also reflects the response of an object to other objects.
####  Identity: It gives a unique name to an object and enables one object to interact with other objects.

![](https://media.geeksforgeeks.org/wp-content/uploads/Blank-Diagram-Page-1-5.png)

#### Declaring Objects (Also called instantiating a class)
####  When an object of a class is created, the class is said to be instantiated. All the instances share the attributes and the behavior of the class. But the values of those attributes, i.e. the state are unique for each object. A single class may have any number of instances.

### Example:
![](https://media.geeksforgeeks.org/wp-content/uploads/Blank-Diagram-Page-1-3.png)
---
## The self
- Class methods must have an extra first parameter in the method definition. We do not give a value for this parameter when we call the method, Python provides it.
- If we have a method that takes no arguments, then we still have to have one argument.
- This is similar to this pointer in C++ and this reference in Java.
####  When we call a method of this object as myobject.method(arg1, arg2), this is automatically converted by Python into MyClass.method(myobject, arg1, arg2) – this is all the special self is about.
---

### __init__ method
#### The __init__ method is similar to constructors in C++ and Java. Constructors are used to initializing the object’s state. Like methods, a constructor also contains a collection of statements(i.e. instructions) that are executed at the time of Object creation. It runs as soon as an object of a class is instantiated. The method is useful to do any initialization you want to do with your object.
---
# Python Testing with pytest: Fixtures and Coverage

## Fixtures
#### When you're writing tests, you're rarely going to write just one or two. Rather, you're going to write an entire "test suite", with each test aiming to check a different path through your code. In many cases, this means you'll have a few tests with similar characteristics, something that pytest handles with "parametrized tests".

####  But in other cases, things are a bit more complex. You'll want to have some objects available to all of your tests. Those objects might contain data you want to share across tests, or they might involve the network or filesystem. These are often known as "fixtures" in the testing world, and they take a variety of different forms.

####  In pytest, you define fixtures using a combination of the pytest.fixture decorator, along with a function definition. For example, say you have a file that returns a list of lines from a file, in which each line is reversed:
---

## Coverage
#### This is all great, but if you've ever done any testing, you know there's always the question of how thoroughly you have tested your code. After all, let's say you've written five functions, and that you've written tests for all of them. Can you be sure you've actually tested all of the possible paths through those functions?

#### For example, let's assume you have a very strange function, only_odd_mul, which multiplies only odd numbers:


#### def only_odd_mul(x, y):
####    if x%2 and y%2:
####        return x * y
####    else:
####        raise NoEvenNumbersHereException(f'{x} and/or {y}
####  ↪not odd')

---

### Summary
#### If you haven't guessed from my three-part focus on pytest, I've been bowled over by the way this testing system has been designed. After years of hanging my head in shame when talking about testing, I've started to incorporate it into my code, including in my online "Weekly Python Exercise" course. If I can get into testing, so can you. And although I haven't covered everything pytest offers, you now should have a good sense of what it is and how to start using it.
---
### references :
---
[geeksforgeeks](https://www.geeksforgeeks.org)
[linuxjournal](https://www.linuxjournal.com/content/python-testing-pytest-fixtures-and-coverage)
