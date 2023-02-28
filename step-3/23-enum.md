# 23: Enum

### Enum

Enum (or enumeration) is a data type that allows developers to create a set of named values. It's similar to a C-style enum, where a unique set of named values is assigned an associated number.

* A Solidity `enum` can be declared as follows:

```solidity
enum Colors {  
    Red,  
    Green,  
    Blue
}
```

This defines a Colors enum with three values: Red, Green, and Blue. Those values will correspond to numbers 0, 1, and 2, respectively.

* Enums can also be used to represent Boolean values:

```solidity
enum Boolean {  
    False,  
    True
}
```

Here, False corresponds to 0 and True corresponds to 1.

* Enums can also be used to represent more complex types:

```solidity
enum ActionType {  
    Buy,  
    Sell,  
    Trade
} 

struct Action {  
    address sender;  
    ActionType type;  
    uint256 amount;
}
```

In this example, the Action struct contains an ActionType field. This allows us to track an action's type (eg, Buy, Sell, or Trade) as a named value.

Enums are a powerful and useful tool for structuring data in Solidity. They allow developers to create a set of named values, which can then be used to represent complex types.

***

### Import Enum - by some examples

The import Enum statement allows you to make use of an existing enum type, in order to give your contracts access to a predefined set of constants. This can be a useful way of providing a limited set of options to a contract, while also avoiding the need to manually define and maintain each individual constant.

In this article, we'll look at a few examples of how to use import Enum to give your contracts access to a predefined set of constants.

* Example 1: Importing an Enum from Another Contract Let's say we have a contract called MyContract, and we want to use an enum type from another contract. We can do this using the following statement:

```solidity
import "./OtherContract.sol"; 
contract MyContract {   
    enum Color { Red, Green, Blue }   Color color;     

    function setColor(Color _color) public {      
        color = _color;   
    }
}
```

In this example, we're importing an enum type from the OtherContract contract, and then using it to define a Color enum in our MyContract contract. We can then use this enum to set the color variable to one of the three predefined colors.

* Example 2: Importing an Enum from a Library We can also use an import Enum statement to give our contract access to an enum type defined in a library. For example, let's say we have a library called MyLib, which defines a Direction enum:

```solidity
library MyLib {   
    enum Direction { North, South, East, West }
}
```

We can then use the following statement to import this enum type into our contract:

```solidity
import "./MyLib.sol"; 
contract MyContract {   
    using MyLib for Direction;   
    Direction direction;      
    function setDirection(Direction _direction) public {      
        direction = _direction;   
    }
}
```

In this example, we're using the using statement to give our contract access to the Direction enum type defined in the MyLib library. We can then use this enum type to set the direction variable to one of the four predefined directions.

* Example 3: Importing an Enum from an External Source Finally, we can also use an import Enum statement to give our contract access to an enum type defined in an external source. For example, let's say we want to use the Weekday enum defined in the Ethereum Foundation's Solidity Standard Library:

```solidity
import "ethereum/solidity-stdlib/Weekday.sol"; 
contract MyContract {   
    using Weekday for Weekday;   
    Weekday day;      
    function setDay(Weekday _day) public {      
        day = _day;   
    }
}
```

In this example, we're using the import statement to give our contract access to the Weekday enum type defined in the Solidity Standard Library. We can then use this enum type to set the day variable to one of the seven predefined weekdays.

### Conclusion

The import Enum statement is a useful way of giving your contracts access to a predefined set of constants, without having to manually define and maintain each individual constant. In this article, we've seen a few examples of how to use import Enum to import an enum type from another contract, from a library, or from an external source.

_That's it for the lesson 23! In the next lesson, Structs_
