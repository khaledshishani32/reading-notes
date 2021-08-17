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



