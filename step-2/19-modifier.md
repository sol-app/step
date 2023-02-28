# 19: Modifier

A modifier is a keyword used to change the behavior of a function or a contract. Modifiers allow you to define a set of conditions that must be met before the function is executed. Modifiers can be used to restrict access to certain functions or to enforce business logic. Here are some examples of how modifiers can be used.

* Example 1: Restrict Access In this example, we will create a modifier to restrict access to a function. This modifier will require the caller of the function to have a certain role.

```solidity
modifier onlyAdmin {  
    require(msg.sender.role == admin);  
    _;
}

function doSomething() onlyAdmin {  // Do something }
```

In this example, the onlyAdmin modifier will check to see if the sender of the function call has the admin role. If the sender does not have the admin role, the function call will be prevented from executing.

* Example 2: Enforce Business Logic In this example, we will create a modifier to enforce a business logic rule. This modifier will check to see if the value of a parameter is within a certain range.

```solidity
modifier withinRange(uint min, uint max) {  
    require(min <= max);  
    require(min <= myValue && myValue <= max);  
    _;
} 

function doSomething(uint myValue) withinRange(100, 200) {// Do something}
```

In this example, the withinRange modifier will check to see if the myValue parameter is between 100 and 200. If myValue is outside of this range, the function call will be prevented from executing.

Modifiers are a powerful tool that can be used to restrict access to certain functions and enforce business logic rules. They can help make your contracts more secure and reliable.

_That's it for the lesson 19! In the next lesson, Constructor_
