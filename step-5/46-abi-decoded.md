# 46: ABI Decoded

An Application Binary Interface (ABI) is a set of rules that defines how two separate pieces of software communicate with each other. It's a set of functions, data types, and protocols that allow two separate pieces of software to interact. In the context of Solidity, ABIs are used to define how smart contracts interact with the Ethereum blockchain.

* Example 1: Storing Data Consider a simple example of a smart contract that stores a value. The contract looks like this:

```solidity
contract StoreValue {  
  uint public value; 
  function StoreValue() {    value = 0;  } 
  function setValue(uint _value) {    value = _value;  }
}
```

The ABI for this contract looks like this:

```json
[
   {
      "constant":false,
      "inputs":[
         {
            "name":"_value",
            "type":"uint256"
         }
      ],
      "name":"setValue",
      "outputs":[
         
      ],
      "payable":false,
      "stateMutability":"nonpayable",
      "type":"function"
   },
   {
      "constant":true,
      "inputs":[
         
      ],
      "name":"value",
      "outputs":[
         {
            "name":"",
            "type":"uint256"
         }
      ],
      "payable":false,
      "stateMutability":"view",
      "type":"function"
   }
]
```

The ABI defines the contract's functionality, including the data types and functions that can be used to interact with the contract. In this example, the ABI defines two functions: setValue and value. The setValue function takes a uint (an unsigned integer) as an input and sets the value of the contract to the input. The value function returns the current value of the contract.

* Example 2: Transferring Ether Now consider a contract that allows users to transfer Ether between two accounts. The contract looks like this:

```solidity
contract TransferEther {  
  address public from;  
  address public to; 
  function TransferEther(address _from, address _to) {    
    from = _from;    
    to = _to;  
  } 
  function transfer(uint amount) {    
    if (msg.value > amount) {      
      from.transfer(amount);      
      to.transfer(amount);    
    }  
  }
}
```

The ABI for this contract looks like this:

```json
[
   {
      "constant":false,
      "inputs":[
         {
            "name":"amount",
            "type":"uint256"
         }
      ],
      "name":"transfer",
      "outputs":[
         
      ],
      "payable":false,
      "stateMutability":"nonpayable",
      "type":"function"
   },
   {
      "constant":true,
      "inputs":[
         
      ],
      "name":"from",
      "outputs":[
         {
            "name":"",
            "type":"address"
         }
      ],
      "payable":false,
      "stateMutability":"view",
      "type":"function"
   },
   {
      "constant":true,
      "inputs":[
         
      ],
      "name":"to",
      "outputs":[
         {
            "name":"",
            "type":"address"
         }
      ],
      "payable":false,
      "stateMutability":"view",
      "type":"function"
   }
]
```

The ABI defines two functions: transfer and from/to. The transfer function takes a uint (an unsigned integer) as an input and transfers the specified amount of Ether from the from address to the to address. The from and to functions return the from and to addresses respectively.

_That's it for the lesson 46! In the next lesson, Keccak256_
