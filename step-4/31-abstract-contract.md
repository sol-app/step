# 31: Abstract Contract

An abstract contract is a special contract type in Solidity that provides a base contract from which other contracts can be derived. The purpose of an abstract contract is to provide various common and reusable pieces of code that can be used to create new contracts. This makes it easier for developers to create contracts that are more efficient and secure.

* Example 1: A Simple Abstract Contract Below is an example of a simple abstract contract that contains a `greet()` function. This function can be used as a base for other contracts to build upon.

```solidity
contract Abstract {  
  function greet() public virtual {    // Do something here  }
}
```

* Example 2: An Abstract Contract with a State Variable Below is an example of an abstract contract with a state variable. The balance state variable can be used as a base in other contracts.

```solidity
contract Abstract {  
  uint256 public balance;  
  function greet() public virtual {    // Do something here  }
}
```

* Example 3: An Abstract Contract with a Getter Function Below is an example of an abstract contract with a getter function. The getBalance() function can be used as a base in other contracts.

```solidity
contract Abstract { // abstract can be like an interface
  uint256 public balance;  
  function greet() public virtual;
  function getBalance() public view returns (uint256);
}

contract A is Abstract {  
  uint256 public balance;  
  function greet() public virtual {    // Do something here  } 
  function getBalance() public view returns (uint256) {    
    return balance;  
  }
}
```

_That's it for the lesson 31! In the next lesson, Payable_
