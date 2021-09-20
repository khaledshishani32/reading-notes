## Dunder Methods

### What Are Dunder Methods?

#### In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

#### How to Statically Generate Pages with Dynamic Routes

#### In our case, we want to create dynamic routes for blog posts:
```
class NoLenSupport:
    pass

>>> obj = NoLenSupport()
>>> len(obj)
TypeError: "object of type 'NoLenSupport' has no len()"

```
#### To fix this, you can add a __len__ dunder method to your class:

```
class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42
```

### Enriching a Simple Account Class

#### Throughout this article I will enrich a simple Python class with various dunder methods to unlock the following language features:

- Initialization of new objects
- Object representation
- Enable iteration
- Operator overloading (comparison)
- Operator overloading (addition)
- Method invocation
- Context manager support (with statement)


### Object Initialization: __init__

#### Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder:
```
class Account:
    """A simple account class"""

    def __init__(self, owner, amount=0):
        """
        This is the constructor that lets us create
        objects from this class
        """
        self.owner = owner
        self.amount = amount
        self._transactions = []
```

### Object Representation: __str__, __repr__

#### It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

- __repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

- __str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

#### Let’s implement these two methods on the Account class:
```
class Account:
    # ... (see above)

    def __repr__(self):
        return 'Account({!r}, {!r})'.format(self.owner, self.amount)

    def __str__(self):
        return 'Account of {} with starting amount: {}'.format(
            self.owner, self.amount)


```

## Operator Overloading for Merging Accounts: __add__

#### In Python, everything is an object. We are completely fine adding two integers or two strings with the + (plus) operator, it behaves in expected ways:
```
>>> 1 + 2
3

>>> 'hello' + ' world'
'hello world'
```

## Callable Python Objects: __call__

#### You can make an object callable like a regular function by adding the __call__ dunder method. For our account class we could print a nice report of all the transactions that make up its balance:
```
class Account:
    # ... (see above)

    def __call__(self):
        print('Start amount: {}'.format(self.amount))
        print('Transactions: ')
        for transaction in self:
            print(transaction)
        print('\nBalance: {}'.format(self.balance))
```

#### Now when I call the object with the double-parentheses acc() syntax, I get a nice account statement with an overview of all transactions and the current balance:
```
>>> acc = Account('bob', 10)
>>> acc.add_transaction(20)
>>> acc.add_transaction(-10)
>>> acc.add_transaction(50)
>>> acc.add_transaction(-20)
>>> acc.add_transaction(30)

>>> acc()
Start amount: 10
Transactions:
20
-10
50
-20
30
Balance: 80
```

### Conclusion

#### I hope you feel a little less afraid of dunder methods after reading this article. A strategic use of them makes your classes more Pythonic, because they emulate builtin types with Python-like behaviors.

#### As with any feature, please don’t overuse it. Operator overloading, for example, can get pretty obscure. Adding “karma” to a person object with +bob or tim << 3 is definitely possible using dunders—but might not be the most obvious or appropriate way to use these special methods. However, for common operations like comparison and additions they can be an elegant approach.

---
### How do for-in loops work in Python? 

#### At this point we’ve got our Repeater class that apparently supports the iterator protocol, and we just ran a for-in loop to prove it:
```
repeater = Repeater('Hello')
for item in repeater:
    print(item)
```

#### To dispel some of that “magic” we can expand this loop into a slightly longer code snippet that gives the same result:
```
repeater = Repeater('Hello')
iterator = repeater.__iter__()
while True:
    item = iterator.__next__()
    print(item)
```

#### As you can see, the for-in was just syntactic sugar for a simple while loop:

- It first prepared the repeater object for iteration by calling its __iter__ method. This returned the actual iterator object.
- After that, the loop repeatedly calls the iterator object’s __next__ method to retrieve values from it.


### A Simpler Iterator Class : 

#### So here’s an idea: RepeaterIterator returns the same value over and over, and it doesn’t have to keep track of any internal state. What if we added the __next__ method directly to the Repeater class instead?

#### That way we could get rid of RepeaterIterator altogether and implement an iterable object with a single Python class. Let’s try it out! Our new and simplified iterator example looks as follows:
```
class Repeater:
    def __init__(self, value):
        self.value = value

    def __iter__(self):
        return self

    def __next__(self):
        return self.value

```

---
### Python Generators 101 – The Basics 

#### Let’s start by looking again at the Repeater example that I previously used to introduce the idea of iterators. It implemented a class-based iterator cycling through an infinite sequence of values.

#### This is what the class looked like in its second (simplified) version:
```
class Repeater:
    def __init__(self, value):
        self.value = value

    def __iter__(self):
        return self

    def __next__(self):
        return self.value
```
#### If you’re thinking, “that’s quite a lot of code for such a simple iterator,” you’re absolutely right. Parts of this class seem rather formulaic, as if they would be written in exactly the same way from one class-based iterator to the next.

#### This is where Python’s generators enter the scene. If I rewrite this iterator class as a generator, it looks like this:
```
def repeater(value):
    while True:
        yield value
```

### Python Generators That Stop Generating : 

#### Thankfully, as programmer's we get to work with a nicer interface this time around. Generators stop generating values as soon as control flow returns from the generator function by any means other than a yield statement. This means you no longer have to worry about raising StopIteration at all!

#### Here’s an example:
```
def repeat_three_times(value) :
    yield value
    yield value
    yield value
```

