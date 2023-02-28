# 11: Events

Events in Solidity allow you to trigger actions based on specific conditions, and are an essential part of a smart contract's functionality. Events are declared with the event keyword and can have any number of arguments of any type.

Example:

```
event Transfer(address indexed _from, address indexed _to, uint256 _value);
```

This event will emit a log when a transfer of value occurs from one address to another, and this log can be used to trigger other actions. The indexed keyword is used to indicate that the argument should be indexed and stored for efficient lookups.

Events are useful for debugging and for allowing external applications to interact with the smart contract, as logs are stored on the blockchain and can be read and used by external applications.

_That's it for the lesson 11! In the next lesson, Condition_
