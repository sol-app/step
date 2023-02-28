# 38: DelegateCall

DelegateCall is a Solidity feature which allows a function to be called on another contract while preserving the caller's address and associated code. This article will discuss DelegateCall by some examples.

## Example 1

Let's assume we have two contracts:

* Contract A
* Contract B&#x20;

Contract A calls the function doSomething in Contract B using delegatecall.

```solidity
contract A {  
    address contractB;    
    function doSomething() public {    
        contractB.delegatecall(bytes4(keccak256("doSomething")));  
    }
} 

contract B {  
    function doSomething() public {    //Do something  }
}
```

By using delegatecall, the function doSomething in Contract B will be called while preserving the caller's address and associated code. In this example, the address of Contract A will be preserved in the call to Contract B.

## Example 2

Let's assume we have three contracts:

* Contract A
* Contract B
* Contract C

Contract A calls the function doSomething in Contract B using delegatecall. Furthermore, Contract B calls the function doSomethingElse in Contract C using delegatecall.

```solidity
contract A {  
    address contractB;    
    function doSomething() public {    
        contractB.delegatecall(bytes4(keccak256("doSomething")));  
    }
} 

contract B {  
    address contractC;    
    function doSomething() public {    
        contractC.delegatecall(bytes4(keccak256("doSomethingElse")));  
    }
} 

contract C {  
    function doSomethingElse() public {    //Do something else  }
}
```

By using delegatecall, the function doSomething in Contract B will be called while preserving the caller's address and associated code. Furthermore, the function doSomethingElse in Contract C will be called while preserving the address of Contract B and its associated code. Thus, in this example, the address of Contract A will be preserved in the call to Contract C.

_That's it for the lesson 38! In the next lesson, Calling Other Contract_
