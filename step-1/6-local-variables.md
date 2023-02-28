# 6: Local Variables

Local variables in Solidity are variables that are defined within a function or a contract and are only accessible within the scope of that particular function or contract. They are initialized with a value when they're declared and can be changed as the code progresses. Local variables are useful for storing temporary values or intermediate results and can be declared in the same way as any other type of variable.

## Example:

```solidity
contract MyContract {    
    uint256 public count;

    function addOne() public {        
        uint256 localNumber = count + 1;        
        count = localNumber;    
    }
}
```

In the example above, localNumber is a local variable. It is declared within the scope of the `addOne()` function and is only accessible within that function. It is initialized with the value of count + 1 and its value is then used to update count.

_That's it for the lesson 6! In the next lesson, Global Variable_
