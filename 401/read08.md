# List Comprehensions
---
### List Comprehension vs For Loop in Python

### Suppose, we want to separate the letters of the word human and add the letters as items of a list. The first thing that comes in mind would be using for loop.

## Example : Iterating through a string Using for Loop
---
#### h_letters = []

#### for letter in 'human':
####    h_letters.append(letter)

#### print(h_letters)
---
#### When we run the program, the output will be:
---
### ['h', 'u', 'm', 'a', 'n']
#### x inside: global
#### x outside: global
--- 
## Example : Iterating through a string Using List Comprehension
---
#### h_letters = [ letter for letter in 'human' ]
#### print( h_letters)
---
## When we run the program, the output will be:
---
#### ['h', 'u', 'm', 'a', 'n']
---
#### In the above example, a new list is assigned to variable h_letters, and list contains the items of the iterable string 'human'. We call print() function to receive the output.
---
## Syntax of List Comprehension
---
#### [expression for item in list]

![](https://cdn.programiz.com/sites/tutorial2program/files/lc.jpg)
---
## Nested List Comprehensions in Python
#### List Comprehensions are one of the most amazing features of Python. It is a smart and concise way of creating lists by iterating over an iterable object. Nested List Comprehensions are nothing but a list comprehension within another list comprehension which is quite similar to nested for loops

---

![](https://i.ytimg.com/vi/AzKV9NbtNJ0/maxresdefault.jpg)


---
[medium](https://medium.com)
[tutorialspoint](https://www.tutorialspoint.com)
