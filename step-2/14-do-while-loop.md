# 14: Do While Loop

A do while loop is a control flow statement that allows code to be executed repeatedly based on a given condition. The do while loop is similar to a while loop, except that the do while loop evaluates its condition at the bottom of the loop instead of the top. This means that the do while loop will always execute once, even if the condition is false.

Syntax:

```solidity
do {   
    statement(s);
} while(condition);
```

Example:

```solidity
int i = 0; 
do {      
    i++;
} while (i < 5);
```

This will print `0,1,2,3,4`.

Example:

```solidity
int number = 0; 
do {   
    number++;    
    console.log(number); // hardhat component \ console log
} while (number < 5);
```

Output: `12345`

_That's it for the lesson 14! In the next lesson, For Loop_
