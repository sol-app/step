# 4: Control Structures

Control structures are an important part of any programming language, as they allow you to specify the flow of execution in your program. In Solidity, there are several control structures that you can use to define the behavior of your smart contract.

## Conditional Statements

The most common type of control structure is the conditional statement. In Solidity, you can use the if statement to specify a condition that must be true in order for a block of code to be executed.\
Here's an example:

```solidity
function isEven(uint256 x) public pure returns (bool) { 
    if (x % 2 == 0) { 
        return true; 
    } else { 
        return false; 
    } 
}
```

In this example, we're defining a function that takes an unsigned integer as a parameter and returns a boolean value indicating whether the number is even or odd. We're using an if statement to check whether the number is even (i.e., whether the remainder of the number divided by 2 is 0).

Solidity also supports the else if and else keywords, which you can use to specify additional conditions or a default behavior:

```solidity
function isPositive(uint256 x) public pure returns (bool) { 
    if (x > 0) { 
        return true; 
    } else if (x == 0) { 
        return false; 
    } else { 
        revert("Number is negative"); 
    } 
}
```

In this example, we're checking whether the number is positive, zero, or negative. If the number is negative, we're reverting the transaction (i.e., canceling it and returning the gas to the sender).

## Loops

Another important type of control structure is the loop. In Solidity, you can use the for, while, and do-while loops to iterate over a block of code. Here's an example of a for loop:

```solidity
function sum(uint256[] memory numbers) public pure returns (uint256) { 
    uint256 total = 0;
    for (uint256 i = 0; i < numbers.length; i++) { 
        total += numbers[i]; 
    } 
    return total; 
}
```

In this example, we're defining a function that takes an array of unsigned integers as a parameter and returns their sum. We're using a for loop to iterate over the array and add up the numbers.

Solidity also supports the while and do-while loops, which you can use to repeat a block of code until a certain condition is met:

```solidity
function countDown(uint256 x) public pure { 
    while (x > 0) {
        x--; 
    } 
} 

functioncountUp(uint256 x) public pure { 
    do { 
        x++; 
    } while (x < 10); 
}
```

In these examples, we're using a while loop to count down from a number and a do-while loop to count up to a number.

## Control Structures with Modifiers

You can also use modifiers to add additional control structures to your Solidity code. For example, you can use a modifier to restrict access to a function:

```solidity
modifier onlyOwner { 
    require(msg.sender == owner); 
    _; 
} 

function changeOwner(address newOwner) public onlyOwner { 
    owner = newOwner; 
}
```

In this example, we're defining a modifier called onlyOwner that checks whether the caller of the function is the owner of the contract. If the caller is the owner, the function executes normally. If not, the function throws an exception.

_That's it for the fourth lesson! In the next lesson, State Variable_
