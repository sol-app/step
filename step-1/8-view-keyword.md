# 8: View Keyword

The view keyword is a modifier used in Solidity to indicate that a function does not modify the state of the contract. It allows the function to call other functions which do not modify the state, while still disallowing other functions which do modify the state.

The view keyword is used to indicate that a function can be executed without changing the state of the contract. This can be used to make the code more efficient, as it allows the compiler to optimize the function.

When the view keyword is used, the function can only read from the contract’s storage, but cannot modify it. This means that the function can access values from storage, but cannot modify them. This is important for ensuring that the function does not accidentally modify data that should remain unchanged.

The view keyword can also be used to make contracts more secure, as it ensures that data cannot be modified accidentally. This can be especially useful when the contract is interacting with external data, as the view keyword helps to ensure that external data is not modified.

For example:

```solidity
contract MyContract {    
    uint256 public myValue; 
    function getMyValue() public view returns (uint256) {        
        return myValue;    
    }
}
```

The `getMyValue()` function is declared with the view keyword, which indicates that it can only be used to read the value of myValue and cannot modify it. This means that it can be called without incurring any gas costs.

_That's it for the lesson 8! In the next lesson, Pure Keyword_
