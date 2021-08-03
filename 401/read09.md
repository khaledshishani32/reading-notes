# Dunder (Magic, Special) Methods and Statistics - Probability
---
### Dunder or magic methods in Python are the methods having two prefix and suffix underscores in the method name. Dunder here means “Double Under (Underscores)”. These are commonly used for operator overloading. Few examples for magic methods are: __init__, __add__, __len__, __repr__ ..
## Example : Iterating through a string Using for Loop
---
## __init__ method
#### The __init__ method for initialization is invoked without any call, when an instance of a class is created, like constructors in certain other programming languages such as C++, Java, C#, PHP etc. These methods are the reason we can add two strings with ‘+’ operator without any explicit typecasting.
![](https://blog.finxter.com/wp-content/uploads/2020/07/pythonint.jpg)

---
## Object Representation: __str__, __repr__

### __str__()
#### This method returns the string representation of the object. This method is called when print() or str() function is invoked on an object.

#### This method must return the String object. If we don’t implement __str__() function for a class, then built-in object implementation is used that actually calls __repr__() function.

### __repr__()
#### Python __repr__() function returns the object representation in string format. This method is called when repr() function is invoked on the object. If possible, the string returned should be a valid Python expression that can be used to reconstruct the object again.
---
## the difference between __str__ and __repr__

- __repr__ goal is to be unambiguous
- __str__ goal is to be readable
- Container’s __str__ uses contained objects’ __repr__

---
## Operator Overloading for Merging Accounts: __add__

####  To perform operator overloading, Python provides some special function or magic function that is automatically invoked when it is associated with that particular operator. For example, when we use + operator, the magic method __add__ is automatically invoked in which the operation for + operator is defined.

![](https://linuxhint.com/wp-content/uploads/2021/01/Operator-Overloading-Python-06.png)

## Python callable and __call__()
#### Python object is called callable if they define __call__() function. If this function is defined then x(arg1, arg2, …) is a shorthand for x.__call__(arg1, arg2, …).

#### Note that callable() function returns True if the object appears callable, it’s possible that it returns True even if the object is not callable. However, if this function returns False then the object is definitely not callable.
---
## Example :

![](https://cdn.journaldev.com/wp-content/uploads/2018/08/python-callable-call-function.png)


---

# Statistics - Probability

#### Statistics is the discipline that concerns the collection, organization, analysis, interpretation, and presentation of data. In applying statistics to a scientific, industrial, or social problem, it is conventional to begin with a statistical population or a statistical model to be studied.

#### Probability is simply how likely something is to happen. Whenever we're unsure about the outcome of an event, we can talk about the probabilities of certain outcomes—how likely they are. The analysis of events governed by probability is called statistics.


![](https://betterexplained.com/wp-content/uploads/2012/09/probability_vs_stats.png)
---
### Three-Sigma 
#### Three-sigma limits is a statistical calculation where the data are within three standard deviations from a mean. In business applications, three-sigma refers to processes that operate efficiently and produce items of the highest quality.
![](http://www.sixsigmadaily.com/wp-content/uploads/sites/4/2012/08/Bell-Curve-Standard-Deviation.jpg)
---
## Z-score
#### The Z-score is a simple calculation that answers the question, “Given a data point, how many standard deviations is it away from the mean?” The equation below is the Z-score equation.

---
### Conclusion
#### We started with descriptive statistics and then connected them to probability. From probability, we developed a way to quantatively show if two groups come from the same distribution. In this case, we compared two wine recommendations and found that they most likely do not come from the same score distribution. In other words, one wine type is most likely better than the other one. Statistics doesn’t have to be a field relegated to just statisticians.

[medium](https://medium.com)
[.dataquest.io](https://www.dataquest.io/blog/basic-statistics-in-python-probability/)
