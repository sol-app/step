# 34: Sending Ether

Ether is the native currency of the Ethereum blockchain, and it can be sent from one address to another. This article will provide some examples of how to send Ether using Solidity.

## Using send

The send function allows you to send Ether from the current contract to an external account. It takes two arguments:

* The recipient address
* The amount of Ether to send

```solidity
function sendEther() public {    
    address recipient = 0x12345...;    
    uint amount = 10 ether;    
    address(this).send(amount);
}
```

**Tips**: dont use `send`

## Using transfer

The transfer function allows you to send Ether from the current contract to an external account. It takes two arguments:

* The recipient address
* The amount of Ether to send

```solidity
function sendEther() public {    
    address recipient = 0x12345...;    
    uint amount = 10 ether;    
    address(this).transfer(recipient, amount);
}
```

## Using call

The call function allows you to execute a function on an external contract. It takes three arguments:

* The address of the external contract
* The data for the function call
* The amount of Ether to send (optional)

```solidity
function sendEther() public {    
    address recipient = 0x12345...;    
    uint amount = 10 ether;    
    address(recipient).call.value(amount)("");
}
```

**Tips**: before using `call` make amount in zero! red more here

_That's it for the lesson 34! In the next lesson, Receive_
