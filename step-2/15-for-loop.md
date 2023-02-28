# 15: For Loop

A for loop is a type of loop that is used in Solidity to execute a set of statements repeatedly until a certain condition is met. The syntax for a for loop is as follows:

```solidity
for (init; condition; increment/decrement) {    
    // Statements to be executed
}
```

**init**: This is an expression that is used to initialize the loop. It is usually an assignment statement.

**condition**: This is the condition that is used to determine whether the loop should be executed or not. If the condition is true, the loop will execute. If the condition is false, then the loop will not execute.

**increment/decrement**: This is an expression that is used to increment or decrement the loop counter.

For example, the following code will print the numbers from 0 to 9:

```solidity
for (uint i = 0; i < 10; i++) {    
    // Print the current value of 'i'    
    Console.log(i); // console log - component of hardhat
}
```

This code will print the numbers from 0 to 9 to the console.

## Basic For Loop

The following is an example of a basic for loop:

```solidity
for (uint i = 0; i < 10; i++) {   // Do something}
```

This code will execute the statements inside the code block 10 times, starting from 0 and incrementing i each iteration.

## For Loop with Multiple Variables

For loops can also be written with multiple variables. This can be done by separating the variables with a comma:

```solidity
for (uint i = 0, uint j = 10; i < 10; i++, j--) {   // Do something}
```

This code will execute the statements inside the code block 10 times, starting from 0 and incrementing i and decrementing j each iteration.

## For Loop with Break Statement

For loops can also be written with a break statement. This can be done by using the break keyword to exit the loop at a certain point.\ For example:

```solidity
for (uint i = 0; i < 10; i++) {   
    // Do something   
    if (i == 5) {      
        break;   
    }
}
```

This code will execute the statements inside the code block 10 times, starting from 0 and incrementing i each iteration. The loop will exit the loop when i reaches 5.

_That's it for the lesson 15! In the next lesson, Required_
