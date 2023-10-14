# 32: Payable

### Payable

Payable is a keyword in Solidity that enables a function to receive Ether. When declaring a function as payable, it indicates that the function is able to receive Ether from external calls.

#### Examples of Payable

* E**xample 1** This is an example of a payable function:

```solidity
function sendEther() public payable {    // Function body}
```

In this example, the `sendEther()` function is declared as a payable function, meaning that it can receive Ether from external calls.

* **Example 2** This is an example of a payable function with a value parameter:

```solidity
function sendEther(uint256 value) public payable {    // Function body}
```

In this example, the `sendEther()` function is declared as a payable function with a parameter of type uint256 representing the amount of Ether to be sent. When this function is called, the value parameter must be specified in order for the function to receive Ether.

**Tips**: for receiving ethers on/in smartcontract, use `receive()` here and/or `fallback()` here.

***

### Payable Address

A `payable address` is an address on the Ethereum blockchain that can receive Ether (ETH) payments. It is important to note that `regular addresses` are not able to `receive payments`, and need to be converted into payable addresses to `receive ETH`.

#### Examples

* Online Wallets Online wallets are a popular way to store, send and receive Ether. These wallets usually come with a feature that allows users to convert a regular address into a payable one. For example, Metamask offers a feature for converting an address into a payable address.
* Smart Contracts Smart contracts are programs that can be deployed to the Ethereum blockchain. They can be used to create payable addresses that can receive payments from other users. For example, the following Solidity code creates a payable address that can receive Ether payments from other users:

```solidity
contract PayableAddress {  
  address payable public payableAddress; 
  constructor() public {    payableAddress = msg.sender;  } 
  fallback() external payable {  // Do something with the received Ether  }
}
```

* MyEtherWallet MyEtherWallet (MEW) is a web-based Ethereum wallet that allows users to easily create, manage and store Ether. It also allows users to convert a regular address into a payable address, which can be used to receive ETH. For example, users can use the `Convert to Payable` feature in MEW to convert an address into a payable one.

***

### Payable Types

Payable types are a special type of data in Solidity that allows for sending Ether to and from smart contracts. This type of data can be used to facilitate transactions between users and contracts, and to enable the transfer of Ether to and from the contract.

#### Examples

* **Example 1**: Sending Ether to the Contract The following example shows how to use the payable keyword to allow users to send Ether to a contract.

```solidity
contract ExampleContract {    
  address public owner;        
  constructor() public {        owner = msg.sender;    }        
  fallback() external payable {  // Logic for contract goes here     }
}
```

In the above code, the `fallback()` is marked as payable. This means that users can send Ether to the contract, and the contract can access it.

**Tips**: function() in oldest version, like fallback() in newst versions

* **Example 2**: Sending Ether from the Contract The following example shows how to use the `payable` keyword to allow a contract to send Ether to a user.

```solidity
contract ExampleContract {    
  address public owner;    

  constructor() public {       
     owner = msg.sender;    
  }   

  function withdrawFunds() public payable {        
    address payable recipient = msg.sender;        
    recipient.transfer(msg.value);     
  }
}
```

In the above code, the `withdrawFunds()` is marked as payable. This means that when a user calls this function, the contract can send Ether to the user.

_That's it for the lesson 32! In the next lesson, Type Data_
