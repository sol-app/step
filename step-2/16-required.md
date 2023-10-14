# 16: Required

Required is a keyword in Solidity that is used to make sure that functions are called with the correct amount of arguments. It will throw an error if the function is called with the wrong number of arguments.

```solidity
contract ExampleContract {    
    function exampleFunction(uint a, uint b) public {        
        require(a > b);    
    }
}
```

In the above example, the require statement ensures that the argument a must be greater than b. If this is not the case, an error is thrown.

* **Example 1** Let's take a look at a simple example of using require to check if a certain value is greater than 0.

```solidity
function checkValue(uint value) public {    
    require(value > 0);    // code executes if value is greater than 0
}
```

In this example, the require statement checks if the value passed to the function is greater than 0. If the value is not greater than 0, the require statement will cause the code to revert and the function will not execute.

* **Example 2** Let's look at another example of using require to check if two values are equal.

```solidity
function checkValues(uint value1, uint value2) public { 
    require(value1 == value2); 
    // code executes if value1 is equal to value2
}
```

&#x20;In this example, the require statement checks if the two values passed to the function are equal. If the values are not equal, the require statement will cause the code to revert and the function will not execute.

_That's it for the lesson 16! In the next lesson, Assert_
