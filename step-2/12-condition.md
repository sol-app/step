# 12: Condition

### If Else Keyword (Condition)

The if else keyword is an important part of Solidity and is used to control the execution of code based on the evaluation of a condition. The keyword is usually used to check for logical conditions, such as checking if a variable is equal to a certain value.

The syntax for an if else statement in Solidity is as follows:

```
if (condition) {    
    // execute this code if condition is true
} else {    
    // execute this code if condition is false
}
```

For example, consider the following code snippet:

```
uint age = 21;
if (age < 18) {    
    // execute this code if age is less than 18
} else {   
     // execute this code if age is greater than or equal to 18
}
```

In this example, the code within the if statement will be executed if the age variable is less than 18, and the code within the else statement will be executed if the age variable is greater than or equal to 18.

***

### Short If

Short if is a shorthand for if-else statements. It is a ternary operator that can be used to shorten an "if-else" statement.

Syntax:

```
condition ? expression1 : expression2;
```

A condition is evaluated to either true or false. If the condition evaluates to true, the expression1 is executed, otherwise expression2 is executed.

Example:

```
int x = 17;
string memory result = (x > 0) ? "positive" : "non-positive";
```

The above statement evaluates the condition `x > 0` and assigns the value "positive" to the result if the condition is true, otherwise assigns the value "non-positive" to the result. Example:

```
int x = 17;
bool res = (x > 0) ? true : false;
```

_That's it for the lesson 12! In the next lesson, While Loop_
