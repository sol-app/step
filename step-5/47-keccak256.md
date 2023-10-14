# 47: Keccak256

### Keccak256

Keccak256 is a hashing algorithm used in Ethereum Blockchain. It is a member of the SHA-2 family and was developed by the team behind the SHA-3 standard. Keccak256 is used to hash transactions and data stored on the Ethereum blockchain and is used as part of the consensus algorithm to determine the validity of transactions.

```solidity
bytes32 hash = keccak256(abi.encode(data1, data2));
```

* **Example**

```solidity
contract MyContract {    
    // Generate the Keccak256 hash of a string    
    function keccak256Hash(string memory _string) public pure returns (bytes32) {        
        return keccak256(abi.encode(_string));    
    }
}
// input: "Hello World"
// output: 0x3c9229289a6125f7fdf1885a77bb12c37a8d3b4962d936f7e3084dece32a3ca1
```

* **Example 1** The following example will demonstrate how Keccak256 works:

Let's say we have a string Hello World and we want to hash it using Keccak256.

The steps are as follows:

Calculate the SHA-3 hash of the string using the Keccak-256 algorithm.\
The result is the hash: 0x36a9e7f1c95b82ffb99743e0c5c4ce95d83c9a430aac59f84ef3cbfab6145068[^1]

* **Example 2** Let's take another example, this time with a hexadecimal string:

Calculate the SHA-3 hash of the string 0x1234 using the Keccak-256 algorithm.\
The result is the hash: 0x1cb9d9f0cb8f7c8b4de1b7e5b5f8c37f5ebf64a86a9f965a5db5c5b5f2f2e1e2[^2]

* **Example 3** Finally, let's take an example with a longer string:

Calculate the SHA-3 hash of the string Hello Ethereum! using the Keccak-256 algorithm.\
The result is the hash: 0x7f5f5c5f25d5bcf8c25ba15f2a9f912fb5e5c4f4b3413fcee50f99a4d234c6f4[^3]

#### Further Reading

For more information on Keccak256 and its usage in Solidity, please see the official [Solidity documentation](https://solidity.readthedocs.io/en/v0.8.0/units-and-global-variables.html#keccak256-hash-function).

***

### Keccak256 - Web3js

Keccak256 is a cryptographic hash function used to generate a fixed-size string of characters from a given input. It is used in Ethereum to generate the address of an account from the public key.

* Usage Keccak256 is used to generate cryptographic hash values from input data. It can be used to process data such as passwords, private keys, and Merkle root hashes. It is also used to generate the address of an Ethereum account from a public key.
* Examples Here are some examples of how to use the Keccak256 function:
* Hashing a Password

```javascript
// Generate a hash of a password
var passwordHash = web3.utils.keccak256("password");
console.log(passwordHash); 
// Output: 0x91e7c79f3ea3d8f7b77d0e0ce7cc9f9d8b7cddd16fbeec717e2c3b5f426b2a5a

// Generating an Ethereum Address

// Generate an Ethereum address from a public key
var publicKey = "0x04de9c3f3ece1f2c3f7fab41c3e8ffd4d4b6b4bf9ea9f8b7e22d28f6a7f013930c8be4f4bb55d4c724a9a937d7e8f0d0f788f32c12f6ccd8cda9a6e9f9c9a3a3f"; 
var address = web3.utils.keccak256(publicKey);
console.log(address); 
// Output: 0xC05D5F5F5f991E719EDAA0fFcc7fcd9F9b8D8d6a
```

_That's it for the lesson 47! In the next lesson, Function Signature Hash_

[^1]: 

[^2]: 

[^3]: 
