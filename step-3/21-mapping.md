# 21: Mapping

### Mapping

Mapping is a data structure in Solidity that allows a programmer to store, retrieve and modify data in a key-value pair format. It is similar to a hash table or dictionary in other languages.

* **Example 1** Let's assume we want to store a list of people and their ages. We can do this with a mapping like this:

```solidity
mapping (address => uint) public peopleAges;
```

* **Example 2** Now, let's assume we want to store a list of people and their names. We can do this with a mapping like this:

```solidity
mapping (address => string) public peopleNames;
```

* **Example 3** Finally, let's assume we want to store a list of people and their ages and names. We can do this with a mapping like this:

```solidity
mapping (address => (uint, string)) public peopleAgesNames;
```

***

### Dynamic Mapping

Dynamic mapping is a data structure in Solidity that allows for variable keys and values. It is used to store data in a key-value format, as in a dictionary.

* **Example 1** Consider the following example:

```solidity
mapping(address => uint) public balances;
```

This creates a mapping from an address to a uint (unsigned integer). This means that each address in the blockchain can have its own integer value. This is useful for tracking balances or other values associated with each address.

* **Example 2** Here is another example:

```solidity
mapping(uint => string) public messages;
```

This creates a mapping from a uint (unsigned integer) to a string. This allows us to store a string value associated with a given integer. This could be used to track messages associated with a particular event or transaction.

* **Example 3** Finally, here is an example using multiple data types:

```solidity
mapping(address => mapping(uint => string)) public userData;
```

This creates a mapping from an address to a mapping of uints to strings. This allows us to store a string value associated with a given address and a given uint. This could be used to store user data associated with a particular address and a particular event or transaction.

_That's it for the lesson 21! In the next lesson, Array_
