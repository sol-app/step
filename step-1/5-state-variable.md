# 5: State Variable

State variables in Solidity are variables that are inside a smart contract. They are stored in the blockchain and their values are persistent and publicly accessible. State variables can be of any data type, such as strings, booleans, integers, and arrays. State variables are typically used to store information about a contract, such as user balances, contract owners, or the current status of a contract.

A state variable can be declared in a smart contract like so:

```solidity
contract MyContract {    
    uint public balance; // Declares a state variable
}
```

State variables can also be declared as private, which means that only functions within the same contract can access them.

```solidity
contract MyContract {    
    uint private balance; // Declares a private state variable
}
```

_That's it for the lesson 5! In the next lesson, Local Variable_
