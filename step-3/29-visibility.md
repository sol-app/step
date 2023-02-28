# 29: Visibility

### Visibility - function scope

Solidity provides four access levels, which are related to the visibility of functions and state variables.\
They are:

#### public:

Everyone can access this, even from outside of the contract.

#### internal:

This can only be accessed from within the same contract or contracts inheriting from it.

#### private:

This can only be accessed from within the same contract.

#### external:

This can only be accessed from outside of the contract.

Examples\
Let's look at a few examples of visibility in action.

Public\
Here's an example of a public variable:

```solidity
contract MyContract {    
    uint public myPublicVariable;
}
```

This variable can be accessed from within the contract, as well as from other contracts and externally.

Internal\
Here's an example of an internal variable:

```solidity
contract MyContract {    
    uint internal myInternalVariable;
}
```

This variable can only be accessed from within the same contract, or from contracts that inherit from it.

Private\
Here's an example of a private variable:

```solidity
contract MyContract {    
    uint private myPrivateVariable;
}
```

This variable can only be accessed from within the same contract.

External\
Finally, here's an example of an external function:

```solidity
contract MyContract {    
    function myExternalFunction() external {        // do something    }
}
```

This function can only be called from outside of the contract.

***

### Visibility Variables

Visibility variables are a concept in Solidity which allow you to control the visibility and access of variables and functions. They are important to keep in mind when creating contracts, as they are used to control the scope of the program.

There are three visibility variables in Solidity:

**Public**: Public visibility allows a variable or function to be visible and accessible both inside and outside the contract.

**Internal**: Internal visibility allows a variable or function to be visible and accessible only within the contract.

**Private**: Private visibility allows a variable or function to be visible and accessible only within the contract but not outside.

#### Examples

Here are some examples of visibility variables in Solidity:

Public

```solidity
contract Example {  
    uint public myVar;  // myVar is publicly accessible    
    function getMyVar() public view returns (uint) {    
        return myVar;  
        // myVar can be accessed both inside and outside the contract  
    }
}
```

Internal

```solidity
contract Example {  
    // myVar is only accessible within the contract    
    uint internal myVar;  
    function getMyVar() internal view returns (uint) {    
        // myVar can only be accessed within the contract  
        return myVar;  
    }
}
```

Private

```solidity
contract Example {  
    // myVar is only accessible within the contract    
    uint private myVar;  
    function getMyVar() private view returns (uint) {    
        // myVar can only be accessed within the contract  
        return myVar;  
    }
}
```

_That's it for the lesson 29! In the next lesson, Interface_
