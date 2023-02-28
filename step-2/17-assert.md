# 17: Assert

Assert is a statement in Solidity that allows for a simple boolean condition to be checked for validity. Assert statements can help to ensure that code is executed as expected.

* Example 1 In this example, we can use an Assert statement to make sure that a function is being called with the expected value:

```solidity
function myFunction(uint _value) public {    
    require(value > 0);    
    assert(_value == 10);    // ...
}
```

In this example, we are using the require statement to make sure that the \_value is greater than 0. We then use the assert statement to make sure that the \_value is equal to 10.

* Example 2 In this example, we can use an Assert statement to make sure that a variable is being set to the expected value:

```solidity
function myFunction(uint _value) public {    
    myVariable = 10;    
    assert(myVariable == 10);    // ...
}
```

In this example, we are setting the myVariable to 10. We then use the assert statement to make sure that the myVariable is equal to 10.

_That's it for the lesson 17! In the next lesson, Revert_
