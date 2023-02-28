# 43: Try and Catch

In Solidity try and catch can be used to handle exceptions. This can prevent a transaction from failing due to an invalid input or a bug in the code.

* Example 1 In the following example, we want to prevent someone from sending more than 5 ether in a single transaction.

```solidity
function sendMoney(address _to, uint256 _amount) public payable {    
    try {        
        require(_amount <= 5 ether);        
        _to.transfer(_amount);    
    } 
    catch (bytes32 err) {        
        revert("Only 5 ether can be sent at a time");    
    }
}
```

In this example, if the \_amount is greater than 5 ether, the require statement will throw an exception and the catch block will handle the exception, reverting the transaction and sending a message to the sender.

* Example 2 In this example, we want to ensure that the sender and receiver are not the same address.

```solidity
function sendMoney(address _to, uint256 _amount) public payable {    
    try {        
        require(_to != msg.sender);        
        _to.transfer(_amount);    
    } 
    catch (bytes32 err) {        
        revert("Sender and receiver cannot be the same address");    
    }
}
```

If the sender and receiver are the same address, the require statement will throw an exception and the catch block will handle the exception, reverting the transaction and sending a message to the sender.

_That's it for the lesson 43! In the next lesson, Library_
