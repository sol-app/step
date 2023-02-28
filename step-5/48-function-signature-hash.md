# 48: Function Signature Hash

A `function signature hash` is a four-byte representation of a function's signature. It is used to uniquely `identify functions` within a contract.

### The following code snippet creates a signature hash using the keccak256 hashing algorithm.

```solidity
contract SignHash {    
    function signHash(string memory message) 
    public view returns (bytes32) {        
        return keccak256(abi.encodePacked(message));    
    }
}
```

* Test

```yaml
string memory message : "getBalance(address)"
Function Name: getBalance
Parameters: address _account
Function Signature: 0x70a08231

string memory message : "getBaltransferance(address,uint256)"
Function Name: transfer
Parameters: address _to, uint256 _value
Function Signature: 0xa9059cbb
```

### The following code snippet creates a signature hash from a transaction.

```solidity
contract SignHash {    
    function signHash(address to, uint256 value, uint256 nonce) 
    public view returns (bytes32) {        
        return keccak256(abi.encodePacked(to, value, nonce));    
    }
}
```

* Example 1: Consider a contract with a function foo(). The signature of the function is foo(). The corresponding signature hash is 0x7f12a5a6.
* Example 2: Consider a contract with a function bar(uint a, string memory b). The signature of the function is bar(uint,string). The corresponding signature hash is 0xacb08c82.
* Example 3: Consider a contract with a function baz(address payable c, uint256 d). The signature of the function is baz(address,uint256). The corresponding signature hash is 0x8b7d828d.

Function Signature Hash A function signature hash is a unique identifier for a function in a smart contract. It is the result of taking the function parameters and hashing them together with a unique algorithm. This hash can then be used to call the function in the future.

For example, consider the following function:

```solidity
function addNumbers(uint a, uint b) public returns (uint) {  
    return a + b;
}
```

The function signature hash of this function is `0x2d2b2ece`. This can be calculated by hashing together the function name (addNumbers) and the parameters (uint a, uint b) using a hashing algorithm such as Keccak-256.

Another example is the following function:

```solidity
function multiplyNumbers(uint a, uint b) public returns (uint) {  
    return a * b;
}
```

The function signature hash of this function is `0xfe710e6f`. This can be calculated by hashing together the function name (multiplyNumbers) and the parameters (uint a, uint b) using a hashing algorithm such as Keccak-256.

_That's it for the lesson 48!_
