# 3: Functions

Functions are an essential part of Solidity smart contracts, as they allow you to define the behavior of the contract. A function can be thought of as a set of instructions that the contract can execute.

## Function Declaration

To declare a function in Solidity, you use the following _syntax_:

```solidity
function functionName(parameter1, parameter2) visibility returns (returnType) { 
    // function body 
}
```

functionName is the name of the function.\
parameter1, parameter2, etc. are the parameters that the function takes (optional).\
visibility specifies the visibility of the function. It can be `public`, `private`, `external`, or `internal` (optional).\
returnType is the data type that the function returns (optional).\
Here's an example of a simple function:

```solidity
function add(uint256 x, uint256 y) public returns (uint256) { 
    return x + y; 
}
```

This function takes two `uint256` parameters and returns their sum.

## Function Visibility

In Solidity, you can specify the visibility of a function using one of four keywords: `public`, `private`, `external`, and `internal`.

`public` functions can be called both internally and externally (i.e., from other contracts and from outside the contract).\
`private` functions can only be called from within the contract.\
`external` functions can only be called from outside the contract.\
`internal` functions can only be called from within the contract or from derived contracts.\
Here's an example of a private function:

```solidity
contract MyContract { 
    uint256 private myNumber; 
    function setNumber(uint256 number) private { 
        myNumber = number; 
    } 
}
```

This function sets the value of myNumber, which is a private variable in the contract. The function is marked as private, which means that it can only be called from within the contract.

## Function Modifiers

A modifier is a special type of function that can be used to modify the behavior of another function. Modifiers can be used to add security checks, to restrict access to a function, or to perform other types of checks before executing the function. Here's an example:

```solidity
modifier onlyOwner { 
    require(msg.sender == owner); 
    _; 
} 

function changeOwner(address newOwner) public onlyOwner { 
    owner = newOwner; 
}
```

In this example, the `onlyOwner modifier` checks whether the caller of the function is the owner of the contract. If the caller is the owner, the function executes normally. If not, the function throws an exception.

## Function Overloading

Solidity supports function overloading, which means that you can define multiple functions with the same name but different parameter lists. Here's an example:

```solidity
function add(uint256 x, uint256 y) public returns (uint256) { 
    return x + y; 
} 

function add(uint256 x, uint256 y, uint256 z) public returns (uint256) { 
    return x + y + z; 
}
```

In this example, we've defined two functions called add with different numbers of parameters. Solidity will be able to distinguish between the two functions based on their parameter lists.

***

_That's it for the third lesson! In the next lesson, we'll cover control structures in Solidity._
