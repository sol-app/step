---
description: Introduction to Solidity
---

# 1: Introduction

### Lesson 1: Introduction to Solidity

Solidity is a contract-oriented programming language used for developing smart contracts on the Ethereum blockchain. Smart contracts are self-executing contracts with the terms of the agreement between buyer and seller being directly written into lines of code. The code and the agreements contained therein exist on a decentralized blockchain network. This makes smart contracts immutable, transparent, and autonomous.

A smart contract is essentially a piece of code that runs on the Ethereum blockchain. The code can interact with other smart contracts and with the Ethereum network as a whole. Smart contracts can be used to automate the transfer of funds, to manage complex workflows, and to enforce business rules.

Here is an example of a simple smart contract written in Solidity:

```solidity
pragma solidity ^0.8.0;
 contract MyContract { 
    string public message; 

    function setMessage(string memory newMessage) public { 
        message = newMessage; 
    } 

    function getMessage() public view returns (string memory) { 
        return message; 
    } 
}
```

This contract is a simple storage contract that allows you to store a message on the Ethereum blockchain. The setMessage function allows you to set the message, and the getMessage function allows you to retrieve the message.

### Let's break down the code:

* The first line (`pragma solidity ^0.8.0;`) specifies the version of Solidity that the code is written in. In this case, we're using version 0.8.0 of Solidity.
* The contract MyContract line defines a new contract called MyContract.
* The string public message line defines a public state variable called message, which is a string.
* The setMessage function takes a string parameter called newMessage, and sets the value of the message state variable to the new message.
* The getMessage function is a read-only function that returns the value of the message state variable.

***

_That's it for the first lesson! In the next lesson, we'll go over data types in Solidity._
