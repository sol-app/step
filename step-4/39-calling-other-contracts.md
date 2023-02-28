# 39: Calling Other Contracts

### Calling Other Contracts

Calling other contracts is an important part of writing Solidity code. It enables you to interact with smart contracts on the Ethereum blockchain from other contracts. In this article, we'll explore a few examples of contract-to-contract interaction and the various ways of calling other contracts.

* Example 1: Calling a Function from Another Contract The most basic way to call a function from another contract is to use the delegatecall keyword. This allows you to call a function from another contract and have the code execute in the context of the calling contract.

Let's look at a simple example. We have two contracts, ContractA and ContractB. ContractA wants to call a function in ContractB:

```solidity
contract ContractA {    
    ContractB b; 
    constructor(ContractB _b) public {    b = _b;    } 
    function callContractB() public {        
        b.delegatecall(bytes4(keccak256("foo()")));    
    } 
} 
contract ContractB {    
    function foo() public {        // Do something    }
}
```

In this example, ContractA calls a function in ContractB using the delegatecall keyword. The delegatecall keyword takes a single argument, which is the function signature of the function to be called. In this example, we are calling the foo() function, so we pass in the function signature as an argument.

* Example 2: Calling a Function from Another Contract with a Return Value In the previous example, we saw how to call a function from another contract without a return value. But sometimes you may want to call a function from another contract and get a return value. To do this, we can use the call keyword.

Let's look at a simple example. We have two contracts, ContractA and ContractB. ContractA wants to call a function in ContractB and get a return value:

```solidity
contract ContractA {    
    ContractB b; 
    constructor(ContractB _b) public {        b = _b;    } 
    function callContractB() public {        
        (bool success, uint256 result) = b.call(
            bytes4(keccak256("foo()"))
        );    
    } 
} 
contract ContractB {    
    function foo() public returns (uint256) {        return 42;    }
}
```

In this example, ContractA calls the foo() function in ContractB using the call keyword. The call keyword takes two arguments, the function signature and a return value. In this example, we are calling the foo() function, so we pass in the function signature as the first argument and the return value as the second argument.

### Conclusion

In this article, we looked at a few examples of contract-to-contract interaction and the various ways of calling other contracts. We saw how to call a function from another contract using the delegatecall keyword and how to call a function from another contract and get a return value using the call keyword.

_That's it for the lesson 39! In the next lesson, Factory Contract_
