# 44: Solidity Library

A Solidity library is a collection of code that can be reused in multiple contracts. This helps to ensure that code is not repeated, and keeps code shorter, cleaner, and easier to maintain.

Here are some examples of how to use a Solidity library:

* **Example 1**: Encoding Suppose you have a contract that needs to encode and decode data as hexadecimal strings. You can create a library to do this, and use it in multiple contracts.

Here is an example of a library for hex encoding:

```solidity
library HexEncoder {    
    // Encode data as hex    
    function encode(bytes data) 
    public view returns (string memory) {        
        // Code for hex encoding    
    } 
    // Decode hex data    
    function decode(string memory data) 
    public view returns (bytes memory) {        
        // Code for hex decoding    
    }
}
```

You can then use this library in other contracts:

```solidity
contract MyContract {    
    using HexEncoder for bytes; 
    function doSomething() public {        
        // Encode data as hex        
        string memory encodedData = HexEncoder.encode(data); 
        // Do something with the encoded data    
    }
}
```

* **Example 2**: Math Suppose you need to do basic math operations in multiple contracts. You can create a library to do this, and use it in multiple contracts.

Here is an example of a library for basic math operations:

```solidity
library Math {    
    // Add two numbers    
    function add(uint a, uint b) public view returns (uint) {    
        return a + b;    } 
    // Subtract two numbers    
    function subtract(uint a, uint b) public view returns (uint) {    
        return a - b;    } 
    // Multiply two numbers    
    function multiply(uint a, uint b) public view returns (uint) {    
        return a * b;    } 
    // Divide two numbers    
    function divide(uint a, uint b) public view returns (uint) {    
        return a / b;    }
}
```

You can then use this library in other contracts:

```solidity
contract MyContract {    using Math for uint; 
    function doSomething() public {        
        // Add two numbers        
        uint result = Math.add(a, b); 
        // Do something with the result    
    }
}
```

_That's it for the lesson 44! In the next lesson, ABI Encoded_
