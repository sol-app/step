# 30: Interface

An interface in Solidity is a collection of function definitions that a contract can implement. An interface is a way for a contract to communicate with other contracts or with external applications.

* **Example 1** This is an example of a basic interface in Solidity:

```solidity
interface MyInterface {    
    function foo(uint a) external returns (uint);    
    function bar(string b) external returns (bool);
}
```

This interface defines two functions: foo and bar. foo takes in a uint (unsigned integer) argument and returns a uint. Similarly, bar takes in a string argument and returns a bool.

* E**xample 2** This is an example of an interface that uses modifiers:

```solidity
interface MyModifiedInterface {    
    modifier onlyOwner {        
        require(msg.sender == owner);        
    _;    
    }

    function foo(uint a) external onlyOwner returns (uint);    
    function bar(string b) external returns (bool);
}
```

In this example, we use a `modifier` called `onlyOwner` to ensure that foo can only be called by the contract's owner. The \_ at the end of the modifier definition indicates that the function should proceed with the rest of its logic after the modifier has been executed.

```solidity
contract A is MyModifiedInterface{
    function foo(uint a) external onlyOwner returns (uint){
        // something only by owner
    }

    function bar(string b) public returns (bool){ 
        // in this example: 'external' change to 'public' by youre usecase
    }
}
```

_That's it for the lesson 30! In the next lesson, Abstract_
