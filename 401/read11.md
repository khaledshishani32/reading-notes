# Data Analysis
---
## What is Jupyter Lab

#### JupyterLab is a web-based interactive development environment for Jupyter notebooks, code, and data. JupyterLab is flexible: configure and arrange the user interface to support a wide range of workflows in data science, scientific computing, and machine learning. JupyterLab is extensible and modular: write plugins that add new components and integrate with existing ones.

![](https://jupyterlab.readthedocs.io/en/stable/_images/jupyterlab.png)


---

## Numpy Tutorial
---
#### NumPy is a Python library used for working with arrays. It also has functions for working in domain of linear algebra, fourier transform, and matrices. NumPy was created in 2005 by Travis Oliphant. It is an open source project and you can use it freely

---

### Numpy 2-Dimensional Arrays

#### With NumPy, we work with multidimensional arrays. We’ll dive into all of the possible types of multidimensional arrays later on, but for now, we’ll focus on 2-dimensional arrays. A 2-dimensional array is also known as a matrix, and is something you should be familiar with. In fact, it’s just a different way of thinking about a list of lists. A matrix has rows and columns. By specifying a row number and a column number, we’re able to extract an element from a matrix.

---

## Array Creation
#### There are several ways to create arrays.

#### For example, you can create an array from a regular Python list or tuple using the array function. The type of the resulting array is deduced from the type of the elements in the sequences.
---
#### >>> import numpy as np
#### >>> a = np.array([2, 3, 4])
#### >>> a
#### array([2, 3, 4])
#### >>> a.dtype
#### dtype('int64')
#### >>> b = np.array([1.2, 3.5, 5.1])
#### >>> b.dtype
#### dtype('float64')
---
## Printing Arrays
#### When you print an array, NumPy displays it in a similar way to nested lists, but with the following layout:
- the last axis is printed from left to right,

- the second-to-last is printed from top to bottom,

- the rest are also printed from top to bottom, with each slice separated from the next by an empty line.

#### One-dimensional arrays are then printed as rows, bidimensionals as matrices and tridimensionals as lists of matrices.
---
#### >>> a = np.arange(6)                    # 1d array
#### >>> print(a)
#### [0 1 2 3 4 5]
#### >>>
#### >>> b = np.arange(12).reshape(4, 3)     # 2d array
#### >>> print(b)
#### [[ 0  1  2]
#### [ 3  4  5]
#### [ 6  7  8]
#### [ 9 10 11]]
#### >>>
#### >>> c = np.arange(24).reshape(2, 3, 4)  # 3d array
#### >>> print(c)
#### [[[ 0  1  2  3]
####  [ 4  5  6  7]
####  [ 8  9 10 11]]

#### [[12 13 14 15]
####  [16 17 18 19]
####  [20 21 22 23]]]

---

## Indexing, Slicing and Iterating
#### One-dimensional arrays can be indexed, sliced and iterated over, much like lists and other Python sequences.
---

#### >>> a = np.arange(10)**3
#### >>> a
#### array([  0,   1,   8,  27,  64, 125, 216, 343, 512, 729])
#### >>> a[2]
#### 8
#### >>> a[2:5]
#### array([ 8, 27, 64])
#### >>> # equivalent to a[0:6:2] = 1000;
#### >>> # from start to position 6, exclusive, set every 2nd element to 1000 
#### >>> a[:6:2] = 1000
#### >>> a
#### array([1000,    1, 1000,   27, 1000,  125,  216,  343,  512,  729])
#### >>> a[::-1]  # reversed a
#### array([ 729,  512,  343,  216,  125, 1000,   27, 1000,    1, 1000])
#### >>> for i in a:
####     print(i**(1 / 3.))

#### 9.999999999999998 
#### 1.0
#### 9.999999999999998
#### 3.0
#### 9.999999999999998
#### 4.999999999999999
#### 5.999999999999999
#### 6.999999999999999
#### 7.999999999999999
#### 8.999999999999998
---
## Reshaping 

#### To change the dimensions of an array, you can omit one of the sizes which will then be deduced automatically:
---
#### >>> a = np.arange(30)
#### >>> b = a.reshape((2, -1, 3))  # -1 means "whatever is needed"
#### >>> b.shape
#### (2, 5, 3)
#### >>> b
#### array([[[ 0,  1,  2],
####    [ 3,  4,  5],
####    [ 6,  7,  8],
####    [ 9, 10, 11],
####    [12, 13, 14]],

####    [[15, 16, 17],
####    [18, 19, 20],
####    [21, 22, 23],
####    [24, 25, 26],
####    [27, 28, 29]]])

---
### references :
---
[Numpy.org](https://numpy.org)
[Dataquest](https://www.dataquest.io)


