# 26: Inheritance

Inheritance is a common _`OOP`_ feature that allows a contract to build on the functionality of another contract. It is a powerful tool for code reuse and code organization, and allows us to build smart contracts with complex behavior.

In Solidity, inheritance works by means of a keyword, is, which is used to indicate that one contract inherits from another.

Let's look at an example of inheritance in Solidity:

```solidity
contract A {    
    function foo() public {        // do something    }
} 

contract B is A {    
    function bar() public {        // do something else    }
}
```

Here, the contract B inherits from the contract A. This means that B will have access to the foo() function defined in A. In addition, it will also have its own bar() function.

**Inheritance** can be chained, meaning that a contract can inherit from another contract which itself inherits from yet another contract.

* For example:

```solidity
contract A {    
    function foo() public {        // do something    }
} 

contract B is A {    
    function bar() public {        // do something else    }
} 

contract C is B {    
    function baz() public {        // do something else    }
}
```

Here, the contract `C` inherits from the contract `B`, which in turn inherits from the contract `A`. This means that `C` will have access to the `foo()` and `bar()` functions defined in `A` and `B`, as well as its own `baz()` function.

Inheritance is a powerful tool for code organization and code reuse. It allows us to build complex smart contracts with clean and simple code.

_That's it for the lesson 26! In the next lesson, Shadowing Effect_
