# 20: Constructor

A constructor is a special type of function that is automatically called when the contract is created. Constructors are typically used to set up initial state variables and any other setup that needs to happen when the contract is first created.

* Example 1

```solidity
contract SimpleConstructor {    
    uint public x; 
    constructor(uint _x) public {        
        x = _x;    
    }
}
```

In this example, the constructor takes in a uint and sets it to the contract's x state variable.

* Example 2

```solidity
contract SimpleConstructor {    
    uint public x;    
    string public str; 
    constructor(uint _x, string memory _str) public {        
        x = _x;        
        str = _str;    
    }
}
```

In this example, the constructor takes in a uint and string and sets them to the contract's x and str state variables, respectively.

**Tips**: in oldest version, constructor() defined by contract name.

_That's it for the lesson 20! In the next lesson, Mapping_
