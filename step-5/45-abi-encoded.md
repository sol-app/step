# 45: ABI Encoded

### ABI Encoded

ABI (Application Binary Interface) encoding is a way to represent smart contract data and functions in a binary format that can be read by the Ethereum Virtual Machine (EVM). It is used to store and transmit data between contracts, and also to store and transport function calls. This encoding is necessary for smart contracts to interact with each other and for them to be triggered by outside events.

#### What is ABI Encoding?

ABI encoding is a way to represent data and functions in a binary form that can be read by the Ethereum Virtual Machine (EVM). This encoding is necessary for smart contracts to be able to communicate with each other, as well as for them to be triggered by events from outside sources. ABI encoding is also used to store and transport function calls.

#### How Does ABI Encoding Work?

ABI encoding is a process of taking data and functions and encoding them into a binary form. This binary form is then readable by the Ethereum Virtual Machine (EVM). When a contract is created, it contains the ABI encoded data and functions that are necessary for it to interact with other contracts, as well as to be triggered by external events.

#### Examples of ABI Encoding

Here are a few examples of ABI encoding in action:

**Storing and transmitting data between contracts**: A smart contract can store and transmit data between contracts using ABI encoding. For example, a contract may use ABI encoding to store and transmit information about a transaction.

**Storing and transporting function calls**: ABI encoding is also used to store and transport function calls. For example, a contract may use ABI encoding to store and transport the function call for transferring funds from one account to another.

**Triggering smart contracts**: ABI encoding is also used to trigger smart contracts. For example, a contract may use ABI encoding to trigger a smart contract when an outside event occurs, such as when a payment is received.

#### Example

Let’s say we have a simple smart contract that takes in two parameters and adds them together. The code for this contract looks like this:

```solidity
contract Adder {    
    function add(uint a, uint b) public returns (uint c) {        
        c = a + b;    
    }
}
```

Now, let’s say we want to call the add() function with the parameters 3 and 5. The ABI-encoded string for this call would look like this:

_0x2a24dbf700000...00000300000...000005_

The `0x2a24dbf7` is the ABI-encoded function signature for the add() function. The rest of the string is the ABI-encoded parameters.

Once we have the ABI-encoded string, we can use it in the call command to call the add() function with the parameters 3 and 5:

```javascript
web3.eth.call({
    to: '<contract address>', 
    data: '0x2a24dbf700000000000000000000000000000000000000000000000000000000000000030000000000000000000000000000000000000000000000000000000000000005'
});
```

### Conclusion

ABI encoding is a powerful tool that allows us to call a smart contract in Ethereum. It is done by generating an ABI-encoded string containing the function name and the parameters we want to pass. Once we have the ABI-encoded string, we can use it in the call command or the sendTransaction command to interact with the smart contract.

_That's it for the lesson 45! In the next lesson, ABI Decoded_
