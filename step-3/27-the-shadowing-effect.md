# 27: The Shadowing Effect

The shadowing effect is an important concept in solidity that explains how changes to a variable's value can have unintended consequences. This is due to the fact that variables in solidity can be shadowed, meaning they can be declared multiple times within the same scope with the same name, but with different values. This can lead to unexpected results, particularly when the variable is used in a function.

* **Example 1** Let's look at the following code:

```solidity
uint x = 10;  
function increaseByTwo() public {   x = x + 2; }
```

If the function increaseByTwo is called, the value of x will be increased by two. This is because the variable x declared within the function has the same name as the one declared outside the function, but has a different value.

* **Example 2** Let's look at the following code:

```solidity
uint x = 10;  
function increaseByTwo() public {   
    uint x = 12;   
    x = x + 2; 
}
```

If the function increaseByTwo is called, the value of x will remain the same. This is because the variable x declared within the function shadows the one declared outside of it, meaning the function is using the value of the x declared within the function, rather than the one declared outside the function.

_That's it for the lesson 27! In the next lesson, Super Keyword_
