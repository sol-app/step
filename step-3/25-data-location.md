# 25: Data Location

### Data Location

Data Location is a concept within Solidity, which refers to the memory or storage locations where data is stored. Knowing where data is located can help you write more efficient smart contracts.

#### Memory

Memory is a volatile location where data is stored temporarily while a function is being executed. All data stored in memory is automatically cleared once the function ends.

* Example:

```solidity
function addTwo(uint a, uint b) public pure returns (uint) {    
    uint c = a + b; // c is stored in memory    
    return c;
}
```

#### Storage

Storage is a persistent location where data is stored on the blockchain. Data stored in storage is accessible and modifiable until a contract is destroyed or removed from the blockchain.

* Example:

```solidity
uint public num; // num is stored in storage  
function setNum(uint a) public {    
    num = a; // set num in storage
}
```

***

### Stack Data Location

In Solidity, data location refers to the place where the data is stored. It can be either storage, memory, or calldata.

**Storage** is the permanent storage area for a contract’s data. All data stored in storage will persist until it is explicitly deleted.

**Memory** is a temporary storage area. It is volatile, meaning that the data is lost when the function call ends.

**Calldata** is the read-only area where the arguments passed to the contract are stored.

Examples:

* Storage

```solidity
contract MyContract {    
    uint256 public value;        
    function setValue(uint256 _value) public {        
        value = _value; // value is stored in storage    
    }
}
```

* Memory

```solidity
contract MyContract {    
    uint256 public value;        
    function setValue(uint256 _value) public {        
        uint256 tempValue = _value; // tempValue is stored in memory        
        value = tempValue;    
    }
}
```

* Calldata

```solidity
contract MyContract {    
    uint256 public value;        
    function setValue(uint256 _value) public {        
        value = _value; // _value is stored in calldata    
    }
}
```

_That's it for the lesson 25! In the next lesson, Inheritance_
