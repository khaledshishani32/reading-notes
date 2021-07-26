# Read & Write Files in Python

---

### Files are named locations on disk to store related information. They are used to permanently store data in a non-volatile memory (e.g. hard disk).

### Since Random Access Memory (RAM) is volatile (which loses its data when the computer is turned off), we use files for future use of the data by permanently storing them.

### When we want to read from or write to a file, we need to open it first. When we are done, it needs to be closed so that the resources that are tied with the file are freed.

### Hence, in Python, a file operation takes place in the following order:

- Open a file
- Read or write (perform operation)
- Close the file
 

## Opening Files in Python
### Python has a built-in open() function to open a file. This function returns a file object, also called a handle, as it is used to read or modify the file accordingly.

### >>> f = open("test.txt")    # open file in current directory
### >>> f = open("C:/Python38/README.txt")  # specifying full path

### We can specify the mode while opening a file. In mode, we specify whether we want to read r, write w or append a to the file. We can also specify if we want to open the file in text mode or binary mode.
---
# Closing Files in Python
### When we are done with performing operations on the file, we need to properly close the file.

### Closing a file will free up the resources that were tied with the file. It is done using the close() method available in Python.

### Python has a garbage collector to clean up unreferenced objects but we must not rely on it to close the file.

### f = open("test.txt", encoding = 'utf-8')
### f.close()

## A safer way is to use a try...finally block.
### try:
###  f = open("test.txt", encoding = 'utf-8')
### finally:
###    f.close()

### This way, we are guaranteeing that the file is properly closed even if an exception is raised that causes program flow to stop.

### The best way to close a file is by using the with statement. This ensures that the file is closed when the block inside the with statement is exited.

### We don't need to explicitly call the close() method. It is done internally.

### with open("test.txt", encoding = 'utf-8') as f:
---
# Writing to Files in Python
### In order to write into a file in Python, we need to open it in write w, append a or exclusive creation x mode.

### We need to be careful with the w mode, as it will overwrite into the file if it already exists. Due to this, all the previous data are erased.

### Writing a string or sequence of bytes (for binary files) is done using the write() method. This method returns the number of characters written to the file.
---
### with open("test.txt",'w',encoding = 'utf-8') as f:
###   f.write("my first file\n")
###   f.write("This file\n\n")
###   f.write("contains three lines\n")

### This program will create a new file named test.txt in the current directory if it does not exist. If it does exist, it is overwritten.

### We must include the newline characters ourselves to distinguish the different lines.
---

# Reading Files in Python

### To read a file in Python, we must open the file in reading r mode.

### There are various methods available for this purpose. We can use the read(size) method to read in the size number of data. If the size parameter is not specified, it reads and returns up to the end of the file.

### We can read the text.txt file we wrote in the above section in the following way:

##### >>> f = open("test.txt",'r',encoding = 'utf-8')
##### >>> f.read(4)    # read the first 4 data
#### 'This'

##### >>> f.read(4)    # read the next 4 data
##### ' is '

##### >>> f.read()     # read in the rest till end of file
##### 'my first file\nThis file\ncontains three lines\n'

##### >>> f.read()  # further reading returns empty sting
##### ''

#### We can see that the read() method returns a newline as '\n'. Once the end of the file is reached, we get an empty string on further reading




---
### references :
---
[programiz](https://www.programiz.com/python-programming/)
[Google](https://www.google.com)
