# Python - Random Module


---

### The random module is a built-in module to generate the pseudo-random variables. It can be used perform some action randomly such as to get a random number, selecting a random elements from a list, shuffle elements randomly, etc.
## Generate Random Floats

### The random.random() method returns a random float number between 0.0 to 1.0. The function doesn't need any arguments.

### Example: random() 
---
#### >>> import random
#### >>> random.random()
#### 0.645173684807533
---

## Generate Random Integers
### The random.randint() method returns a random integer between the specified integers.

## Example: randint() 
---
#### >>> import random
#### >>> random.randint(1, 100)
#### 95           
#### >>> random.randint(1, 100)
#### 49
---
## Generate Random Numbers within Range
### The random.randrange() method returns a randomly selected element from the range created by the start, stop and step arguments. The value of start is 0 by default. Similarly, the value of step is 1 by default.

## Example: 
---
#### >>> random.randrange(1, 10)
#### 2
#### >>> random.randrange(1, 10, 2)
#### 5            
#### >>> random.randrange(0, 101, 10)
#### 80
---
## Select Random Elements
### The random.choice() method returns a randomly selected element from a non-empty sequence. An empty sequence as argument raises an IndexError.

## Example: 
---

#### >>> import random
#### >>> random.choice('computer')
#### 't'          
#### >>> random.choice([12,23,45,67,65,43])
#### 45           
#### >>> random.choice((12,23,45,67,65,43))
#### 67
---

## Shuffle Elements Randomly
### The random.shuffle() method randomly reorders the elements in a list.

## Example: 
---
#### >>> numbers=[12,23,45,67,65,43]
#### >>> random.shuffle(numbers)
#### >>> numbers
#### [23, 12, 43, 65, 67, 45]
#### >>> random.shuffle(numbers)
#### >>> numbers
#### [23, 43, 65, 45, 12, 67]
---

# What is Risk Analysis

#### Risk analysis in software testing is an approach to software testing where software risk is analyzed and measured. Traditional software testing normally looks at relatively straight-forward function testing (e.g. 2 + 2 = 4). A software risk analysis looks at code violations that present a threat to the stability, security, or performance of the code.

#### Software risk is measured during testing by using code analyzers that can assess the code for both risks within the code itself and between units that must interact inside the application. The greatest software risk presents itself in these interactions.  Complex applications using multiple frameworks and languages can present flaws that are extremely difficult to find and tend to cause the largest software disruptions.

---
### Why Perform Risk Analysis in Software Testing?
#### Because finding defects in production is expensive! The key reason why people perform risk analysis during software testing is to better understand what can really go wrong with an application before it goes into production. A risk analysis performed during software testing helps to identify areas where software flaws could result in serious issues in production. By identifying areas of concern early, developers are able to proactively remediate and reduce the overall risk of a production defect.
---
### Implementing Risk Analysis in Software Testing
#### Implementing risk analysis in software testing typically requires a detailed evaluation of the source code to identify how it interacts with other components of a complete application. This evaluation looks at the various code components and maps how the code interacts. With this map, transactions can be identified and evaluated. Architectural and structural rules can be applied to the map to understand where software flaws lie and which ones are the most important given the transactions flowing through the application.

---
### references :
---
[castsoftware](https://www.castsoftware.com)

[tutorialspoint](https://www.tutorialspoint.com)
