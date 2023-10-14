# 35: Receive

### Receive()

Receive is a special function in Solidity that allows contracts to receive funds from external accounts.

* **Example 1** Below is a simple example of how to use `receive()` to accept ether:

```solidity
contract MyContract {    // Receive Ether    
    receive() external payable { // Do something with the received ether }
}
```

* **Example 2** The receive function can also be used to accept tokens. Here is an example of how to receive ERC20 tokens:

```solidity
import "./token.sol"; // A standard ERC20 token 
contract MyContract {    
    Token token; 
    constructor(address _tokenAddress) {        
        token = Token(_tokenAddress);    
    } 
    // Receive ERC20 tokens    
    receive() external {        
        uint256 amount = msg.value;        
        token.transferFrom(msg.sender, address(this), amount);    
    }
}
```

* **Example 3** The receive() function can also be used to accept both Ether and ERC20 tokens. Here is an example of how to do this:

```solidity
import "./token.sol"; // A standard ERC20 token 
contract MyContract {    
    Token token; 
    constructor(address _tokenAddress) {        
        token = Token(_tokenAddress);    
    } 
    // Receive Ether and ERC20 tokens    
    receive() external payable {        
        uint256 amount = msg.value;        
        if (msg.value > 0) { // Receive ether            
            // Do something with the received ether        
        }        
        else {            // Receive tokens            
            token.transferFrom(msg.sender, address(this), amount);        
        }    
    }
}
```

***

### 'recieve()' Hack - By Some Examples

The 'recieve()' function in Solidity is a powerful tool that can be used to both facilitate and exploit the Ethereum network.

This function allows users to send ETH to a contract and it will be stored in the contract's balance.

### Exploiting the 'recieve()' Function

This function is often exploited by attackers as it allows them to inject malicious code into contracts and drain the ETH balance.

For example, an attacker can craft a malicious transaction and send it to a contract's address, which then calls the 'recieve()' function and executes their code. This code can then access the contract's ETH balance and drain it.

### Securing the 'recieve()' Function

In order to secure the 'recieve()' function, developers should ensure that the code within the function is secure and only allows certain transactions to take place.

For example, developers can use a whitelist of addresses that are allowed to transfer funds to the contract's balance, and only allow transactions from those addresses. This will prevent malicious actors from sending malicious code to the contract.

**Tips**: In addition, developers should also audit the code within the 'recieve()' function to ensure that it is secure and does not contain any exploitable vulnerabilities.

_That's it for the lesson 35! In the next lesson, Fallback_
