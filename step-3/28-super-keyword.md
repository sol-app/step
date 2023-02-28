# 28: Super Keyword

The super keyword is used to access the functions and members of the parent class in Solidity. It is similar to `this` keyword in other languages.

* Example 1

```solidity
contract A {    
    function f() {        // ...    }
} 

contract B is A {    
    function g() {        
        // This will call function f of contract A        
        super.f();    
    }
}
```

* Example 2

```solidity
contract A {    
    string public x;    
    function f() {        // ...    }
}

contract B is A {    
    function g() {        
        // This will access the public variable x of contract A        
        string y = super.x;    
    }
}
```

_That's it for the lesson 28! In the next lesson, Visibility_
