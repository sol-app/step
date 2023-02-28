# 7: Global Variables

Global variables are variables that are **declared outside of any function, class, or contract**. They are available to all functions, classes, and contracts within the same scope. _Tips: some times you declare Error like global variable._

Global variables are declared with the global keyword followed by the type of the variable and its name.\
_`global keyword` censored in solidity_

```solidity
    global uint256 myGlobalVariable;
    
    // OR

    uint256 myGlobalVariable;
    contract Name{
        ...
    }
```

The value of a global variable is initialized with the constructor, and can be modified by any function, class, or contract within the same scope.

```solidity
constructor() public {    
    myGlobalVariable = 0;  
}    

    function setMyGlobalVariable(uint256 _value) public {    
        myGlobalVariable = _value;  
}
```

_That's it for the lesson 7! In the next lesson, View Keyword_
