# 9: Pure Keyword

Solidity provides a special keyword, pure, that can be used to indicate that a function does not alter the state of any of the variables in the contract. This is useful for functions that only return a value based on the inputs, without changing anything else.

A pure function does not:

* Read or write to the blockchain
* Create or send a transaction
* Access any state variables
* Call any other functions

Using the pure keyword provides a guarantee to the compiler that the function won’t alter the state of the contract, which can be used to optimize the code. It also allows the function to be called in constant time, meaning it won’t be affected by the size of the blockchain or the number of transactions.

Example of a _pure function_ in Solidity:

```solidity
function add(uint a, uint b) public pure returns (uint) {  
    return a + b;
}
```

_That's it for the lesson 9! In the next lesson, Constant Keyword_
