# 10: Immunable Keyword

### Constant Keyword

The constant keyword is used to declare a state variable as a constant. It is important to note that a constant can only be assigned a value during its declaration and cannot be changed afterwards.

A constant can also be declared with the view or pure keyword, which allows functions to access the constant without changing its value.

constant in function scoop was depricated.

Example:

```solidity
contract MyContract {    
    uint constant tokenTotalSupply = 100;     

    function getTokenTotalSupply() public view returns (uint) {        
        return tokenTotalSupply;    
    }
}
```

In the above example, tokenTotalSupply is declared as a constant and its value is assigned to 100. The function `getTokenTotalSupply()` is declared as public view and allows external contracts to view the constant without changing its value.

### Introduction to the immutable Keyword

The immutable keyword is a powerful tool in Solidity that allows developers to create data that is protected from tampering. It is a way to ensure that stored data is safe and secure, and that it cannot be changed without explicit authorization.

Example #1

Consider the following code:

```solidity
contract MyContract {    
    uint256 public immutable myNumber; 

    function setMyNumber(uint256 _myNumber) public {        
        myNumber = _myNumber;    
    }
}
```

In this example, the immutable keyword is used to declare a public variable myNumber. This means that the value of myNumber can be read by anyone, but it cannot be changed without using the setMyNumber function.

Example #2

Now consider the following code:

```solidity
contract MyContract {    
    bytes32 public immutable myData; 

    function setMyData(bytes32 _myData) public {        
        myData = _myData;    
    }
}
```

In this example, the immutable keyword is used to declare a public variable myData. This means that the value of myData can be read by anyone, but it cannot be changed without using the setMyData function.

#### Conclusion

The immutable keyword is a powerful tool in Solidity that allows developers to create data that is protected from tampering. By using this keyword, developers can ensure that their data is safe and secure and cannot be changed without explicit authorization.

_That's it for the lesson 10! In the next lesson, Event_
