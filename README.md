---
description: From zero to hero
---

# Learning Solidity

### Explain Smart contract

A smart contract is **an agreement between two people or entities in the form of computer code programmed to execute automatically**. The idea was proposed in the 1990s by `Nick Szabo`, a pioneer of modern computer science, who defined them as a set of virtual promises with associated protocols to enforce them.

Smart contracts are executed on blockchain, which means that the terms are stored in a distributed database and cannot be changed. Transactions are also processed on the blockchain, which automates payments and counterparties. Since the emergence of the digital currency Ethereum, the creation and execution of smart contracts has been simplified, as complex transactions can be programmed into the Ethereum protocol.

### Explain Solidity language

Solidity is **an object-oriented programming language created specifically by the Ethereum Network team for constructing and designing smart contracts on Blockchain platforms**.

* It's used to create smart contracts that implement business logic and generate a chain of transaction records in the blockchain system.
* It acts as a tool for creating machine-level code and compiling it on the "Ethereum Virtual Machine" (EVM).
* It has a lot of similarities with C and C++ and is pretty simple to learn and understand. For example, a “main” in C is equivalent to a “contract” in Solidity.

***

Create by Example Creating a contract in solidity involves writing functions and deploying them to the blockchain. Here are some examples of how to create a contract in Solidity:

Simple Storage Contract This is a simple storage contract example that stores a single value:

```solidity
pragma solidity ^0.4.17; 
contract SimpleStorage { 
	uint storedData; 
	function set(uint x) public { storedData = x; } 
	function get() public view returns (uint) { return storedData; }
}
```

Payable Contract This is an example of a payable contract that allows users to send ether to the contract. The contract then stores the amount of ether received.

```solidity
pragma solidity ^0.4.17; 
contract Payable { 
	uint storedData; 
	function payable(uint x) public payable { storedData = x; } 
	function get() public view returns (uint) { return storedData; }
}
```

Token Contract This is an example of a token contract that allows users to transfer tokens between accounts.

```solidity
pragma solidity ^0.4.17; 
contract Token { 
	mapping (address => uint) public balances; 
	function transfer(address _to, uint _value) public { 
		require(balances[msg.sender] >= _value); balances[msg.sender] -= _value; balances[_to] += _value; 
	}
}
```

&#x20;By using these examples, you can get started creating your own contracts in Solidity.

***

{% hint style="info" %}
Using search (_**top right of window**_) : the Ai help you for your question.

Ai using this website internal data.
{% endhint %}

***

| LESSONS                     |                        |
| --------------------------- | ---------------------- |
| Smart Contract Language     | Remix Id Tutorial      |
| Write You First Contract    | Solidity Data Type     |
| Solidity Function           | State variable         |
| Local Variable              | Global variable        |
| View Keyword                | Pure Keyword           |
| Event Ticket Smart Contract | Constant Keyword       |
| If Else Keyword             | while loop             |
| Do Wile Loop                | For Loop               |
| Required Error              | Assert Error           |
| Revert Error                | Modifier               |
| Constructor                 | Mapping                |
| Array                       | Array Remove           |
| Replace Array               | Enum Solidity          |
| Import Enum                 | Structs                |
| Import Structs              | Data Location          |
| Solidity Events             | Inheritance            |
| Shadowing Effect            | Super Keyword          |
| Visibility Solidity         | Interface Solidity     |
| Payable                     | Sending ether solidity |
| fallback                    | Call Function          |
| DelegateCall                | Calling other Contract |
| Create Other Contract       | Try and catch          |
| Solidity Library            | Solidity ABI Encoded   |
| Solidity ABI Decoded        | Keccak256              |
| DAPP                        | . . .                  |

_In the next lesson, we'll go over Introducing Solidity language._
