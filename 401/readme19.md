# Python Regular Expression 
---

#### A regular expression is a special sequence of characters that helps you match or find other strings or sets of strings, using a specialized syntax held in a pattern. Regular expressions are widely used in UNIX world.

#### The Python module re provides full support for Perl-like regular expressions in Python. The re module raises the exception re.error if an error occurs while compiling or using a regular expression.

#### We would cover two important functions, which would be used to handle regular expressions. But a small thing first: There are various characters, which would have special meaning when they are used in regular expression. To avoid any confusion while dealing with regular expressions, we would use Raw Strings as r'expression'.

![](https://blog.finxter.com/wp-content/uploads/2020/11/pythonRegexFullmatch-1024x576.jpg)

### The match Function
#### This function attempts to match RE pattern to string with optional flags.

#### Here is the syntax for this function −
## code :
#### re.match(pattern, string, flags=0)
---

## Example :


#### import re

#### line = "Cats are smarter than dogs"

#### matchObj = re.match( r'(.*) are (.*?) .*', line, re.M|re.I)

#### if matchObj:
####   print "matchObj.group() : ", matchObj.group()
####   print "matchObj.group(1) : ", matchObj.group(1)
####   print "matchObj.group(2) : ", matchObj.group(2)
#### else:
####   print "No match!!"

### matchObj.group() 
#### Output =>  Cats are smarter than dogs
### matchObj.group(1) 
#### Output =>  Cats
### matchObj.group(2)  
#### Output =>  smarter

---

## The search Function
#### This function searches for first occurrence of RE pattern within string with optional flags.

#### Here is the syntax for this function −

#### re.search(pattern, string, flags=0)

---

## Search and Replace
### Syntax
#### re.sub(pattern, repl, string, max=0)

## Eample :

#### import re

#### phone = "2004-959-559 # This is Phone Number"


#### num = re.sub(r'#.*$', "", phone)
#### print "Phone Num : ", num


#### num = re.sub(r'\D', "", phone)    
#### print "Phone Num : ", num
## Output :
#### Phone Num :  2004-959-559
#### Phone Num :  2004959559

---

## Greedy vs. Non-Greedy Matching
#### When a special character matches as much of the search sequence (string) as possible, it is said to be a "Greedy Match". It is the normal behavior of a regular expression, but sometimes this behavior is not desired:
## Code :
#### pattern = "cookie"
#### sequence = "Cake and cookie"

#### heading  = r'<h1>TITLE</h1>'
#### re.match(r'<.*>', heading).group()
### Output :
#### '<h1>TITLE</h1>' 
---
## Python Regular Expression Cheatsheet table :

![](https://cdn.activestate.com/wp-content/uploads/2020/03/Python-RegEx-Cheatsheet-pin-806x2048.jpg)

---
## shutil — High-level File Operations

#### A number of functions for hgh level operations on files and directories have been defined in shutil module of Python’s standard library.

## copy()
#### This function copies a file to a specified file in same or other directory. First parameter to the function is a string representation of existing file. Second argument is either name of resultant file or directory. If it is a directory, the file is coped in it with same name. The metadata of original file is not maintained..

#### >>> import shutil
#### >>> shutil.copy("hello.py","newdir/")
#### 'newdir/hello.py'
---
## copy2()
#### This function is similar to copy() function except for the fact that it retains metadata of source file. For example the date modified property of resulting file will be similar to original file.

#### >>> shutil.copy2('person.py', 'newdir/')
#### 'newdir/person.py'

---
## copyfile()
#### Two string arguments of this function represent file names.It means the original file is copied by the specified name in the same directory.

#### >>> shutil.copyfile('start.py', 'end.py')
#### 'end.py'
---
## copyfileobj()

#### The parameters of this function are file objects rather than strings representing files. The file objects are obtained by open() function. Original file should have read permission and resulting file hould be opened with write permission.

#### >>> f1=open('hello.py','r') 
#### >>> f2=open('python.py','w')
#### >>> shutil.copyfileobj('f1', 'f2')
#### >>> shutil.copyfileobj(f1, f2)
---
## copytree()
#### This function recursively copies file and subdirectories in one directory to another directory. Names of two parameters must be string. Directory of second parameter’s name should not exist earlier. To copy individual files copy2() function is internally used.

#### >>> shutil.copytree('dir1','dir2')
#### 'dir2'
---
## rmtree()
#### This function removes files and subdirectories in the specified directory.
#### >>> shutil.rmtree('dir2')
#### >>> shutil.move('hello.py', 'newdir/')
#### 'newdir/hello.py'
---

## which()
#### This function returns path to an executable.

#### >>> shutil.which('calc')
#### 'C:\\WINDOWS\\system32\\calc.EXE'
---
## make_archive()
#### This function builds an archive (zip or tar) of files in the root directory.

#### >>> root_dir='newdir'
#### >>> shutil.make_archive("newdirarch","zip",root_dir)
#### 'C:\\python36\\newdirarch.zip'
