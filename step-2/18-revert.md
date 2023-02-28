# 18: Revert

Revert is an important keyword in the Solidity programming language. It allows developers to handle errors that occur during execution of a contract. It is used to terminate and revert a contract, and provides a reason for the termination.

Syntax\
The syntax of the `revert` keyword is as follows:

```solidity
revert(message);
```

Where message is an optional string that can be used to provide a reason for the revert.

* Example 1 Below is an example of a contract that uses revert to terminate an execution if a requirement is not met.

```solidity
contract RevertExample {    
    function deposit() public payable {        
        if (msg.value < 100) {            
            revert("Deposit must be at least 100.");        
        }        // ...    
    }
}
```

In this example, the `deposit` function will terminate and revert if the value of the msg.value is less than 100.

* Example 2 Below is an example of a contract that uses revert to terminate an execution if a requirement is not met.

```solidity
contract RevertExample {    
    uint256 private ownerBalance; 
    function withdraw() public {        
        if (msg.value > ownerBalance) {            
            revert("Insufficient funds.");        
        }        // ...    
    }
}
```

In this example, the withdraw function will terminate and revert if the value of the msg.value is greater than the `ownerBalance` variable

_That's it for the lesson 18! In the next lesson, Modifier_
