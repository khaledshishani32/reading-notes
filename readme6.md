# &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Comparison and logical operators:

 ## Comparison operators :
### A comparison operator compares its operands and returns a logical value based on whether the comparison is true. The operands can be numerical, string, logical, or object values .

- Equal (==) Returns true if the operands are equal. compare values between value .
- Not equal (!=) Returns true if the operands are not equal . compare  between values .
- Strict equal (===) Returns true if the operands are equal and of the same type.
- Strict not equal (!==) Returns true if the operands are of the same type but not equal, or are of different type.
- Greater than or equal (>=)	Returns true if the left operand is greater than or equal to the right operand.
- Less than or equal (<=)	Returns true if the left operand is less than or equal to the right     operand.

# &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; Logical operators

### Logical operators are typically used with Boolean (logical) values; when they are, they return a Boolean value. However, the && and || operators actually return the value of one of the specified operands, so if these operators are used with non-Boolean values, they may return a non-Boolean value. The logical operators are described in the following table.

- (&&) Return true if the all exp is true .
- (||) Return true if at least exp is true .
- (!)  Can convert the value from true to fales .
   
# &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  JavaScript Loop



##  &nbsp; &nbsp; While Loop : 

### &nbsp; &nbsp; The while loop loops through a block of code as long as a specified condition is true .

![](https://simplesnippets.tech/wp-content/uploads/2018/10/while-loop-in-javascript-featured-image-1280x720.jpg)

## &nbsp; &nbsp; For Loop :
### &nbsp; &nbsp; &nbsp; &nbsp; The for statement creates a loop that consists of three optional expressions, enclosed in parentheses and separated by semicolons, followed by a statement (usually a block statement) to be executed in the loop.


### Initialization :
### An expression (including assignment expressions) or variable declaration evaluated once before the loop begins. Typically used to initialize a counter variable. This expression may optionally declare new variables with var or let keywords. Variables declared with var are not local to the loop, i.e. they are in the same scope the for loop is in. Variables declared with let are local to the statement.

### Condition :
### An expression to be evaluated before each loop iteration. If this expression evaluates to true, statement is executed. This conditional test is optional. If omitted, the condition always evaluates to true. If the expression evaluates to false, execution skips to the first expression following the for construct.


# &nbsp; &nbsp; Example:
## var str = '';

## for (var i = 0; i < 9; i++) {
##  str = str + i;
## }

## console.log(str);

## References:

[w3schools](https://www.w3schools.com/)
[mozilla](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for)