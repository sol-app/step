# 33: Using type()

`type()` is a function in Solidity that allows developers to query the type of a variable. This can be a useful tool for debugging, as it can help developers identify issues with their code. Here are some examples of using type()

* **Example 1**

```solidity
uint256 myInteger = 5; 
type(myInteger);
```

This will return uint256, as myInteger is declared as a uint256 variable.

* **Example 2**

```solidity
string myString = "Hello World"; 
type(myString);
```

This will return string, as myString is declared as a string variable.

* **Example 3**

```solidity
mapping(uint256 => uint256) myMapping; 
type(myMapping);
```

This will return mapping(uint256 = uint256), as myMapping is declared as a mapping from uint256 to uint256.

_That's it for the lesson 33! In the next lesson, Sending-Ether_
