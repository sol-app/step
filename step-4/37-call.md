# 37: Call

### Call Function

A call function is a type of function in Solidity that sends a message from one contract to another while not creating a transaction on the blockchain. This is useful when you need to read data from a contract without making any changes, as it is faster and costs less gas.

* **Example 1** The following code shows an example of a call function which is used to read the value of a variable myVar from a contract called MyContract:

```solidity
contract Caller {    
    function readMyVar() public view returns (uint) {        
        return MyContract.myVar();    
    }
}
```

* **Example 2** The following code shows an example of a call function which is used to call a function makePayment from a contract called PaymentContract:

```solidity
contract Caller {    
    function makePayment(address _to, uint _amount) public {        
        PaymentContract.makePayment(_to, _amount);    
    }
}
```

***

### Call() Function

The call() function is a powerful tool for Ethereum developers. It allows for sending transactions to other contracts without having to interact with them directly. This is extremely useful for testing, creating transactions that would otherwise be too expensive, or for interacting with contracts that you don't own.

* **Example 1** Let's say we have a contract called MyContract that sends a message to another contract when called. We can call MyContract.call() like this:

```solidity
MyContract.call({  to: <address of other contract>,  data: <data to send>})
```

* E**xample 2** We can also use call() to send Ether to a contract. Let's say we have a contract called MyFund that accepts Ether donations. We can call MyFund.call() like this:

```solidity
MyFund.call({  to: <address of MyFund>,  value: <amount of Ether to send>})
```

* **Example 3** Finally, we can use call() to call other functions of a contract. Let's say we have a contract called MyToken that has a function called transfer() for transferring tokens. We can call MyToken.call() like this:

```solidity
MyToken.call({  
    to: <address of MyToken>,  data: <data for transfer() function>
})
```

Using the call() function can be a powerful way to interact with contracts that you don't own, as well as for testing and creating transactions that would otherwise be too expensive.

_That's it for the lesson 37! In the next lesson, Delegate Call_
