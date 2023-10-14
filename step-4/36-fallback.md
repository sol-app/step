# 36: Fallback

### Fallback()

The `fallback()` function is a special function in Solidity that is used to define a default behavior if no other functions have been called. It is triggered when a contract receives a transaction or message call and no other functions match the given _**signature**_.

* **Example 1** The following example shows a fallback() function that logs a warning message when called.

```solidity
contract MyContract {   
    event LogWarning(string message);
    function () public {        // Log a warning        
        emit LogWarning("You called the fallback function!");    
    }
}
```

* **Example 2** The following example shows a fallback() function that reverts any calls to it with a warning message.

```solidity
contract MyContract {    
    function () public {        // Revert and log a warning        
        revert("You called the fallback function!");    
    }
}
```

* **Example 3** The following example shows a fallback() function that accepts any incoming funds and stores them in an account balance.

```solidity
contract MyContract {    
    uint public balance; 
    function () public payable {        // Store incoming funds        
        balance += msg.value;    
    }
}
```

***

### fallback() Hack - by Some Examples

The `fallback()` function is a special function in Solidity that can be used to catch any incoming transaction or call to a contract that hasn't been defined or declared by a user. It is a powerful tool, and can be used to execute malicious code if used without proper caution.

Here are some examples of how it can be used:

* **Example 1** In this example, we will use the fallback function to send any Ether that is sent to the contract to the calling address.

```solidity
contract FallbackExample {    
    address public owner; 
    constructor() public {        owner = msg.sender;    } 
    fallback() external payable {        
        require(msg.sender != address(0));        
        owner.transfer(msg.value);    
    }
}
```

* **Example 2** In this example, we will use the fallback function to increase the balance of the calling address by 10% of the amount that was sent to the contract.

```solidity
contract FallbackExample {    
    address public owner; 
    constructor() public {        owner = msg.sender;    } 
    fallback() external payable {        
        require(msg.sender != address(0));        
        owner.transfer(msg.value + (msg.value * 0.1));    
    }
}
```

* **Example 3** In this example, we will use the fallback function to execute an arbitrary function when a transaction is sent to the contract.

```solidity
contract FallbackExample {    
    address public owner; 
    constructor() public {        owner = msg.sender;    } 
    fallback() external payable {        
        require(msg.sender != address(0));        
        executeArbitraryFunction();    
    } 
    function executeArbitraryFunction() internal { // Arbitrary code here }
}
```

**Tips**: In addition, developers should also audit the code within the 'fallback()' function to ensure that it is secure and does not contain any exploitable vulnerabilities.

_That's it for the lesson 36! In the next lesson, Call Function_
