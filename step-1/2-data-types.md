# 2: Data Types

In Solidity, like in many programming languages, variables have a data type that determines the kind of value that can be stored in the variable. Solidity supports a variety of data types, including:

* Boolean: bool
* Integer: int and uint of various sizes
* Address: address
* Bytes: bytes and byte
* String: string
* Arrays: array
* Structs: struct
* Enumerations: enum Let's take a closer look at each of these data types.

## Boolean

The bool type in Solidity can have one of two values: true or false. It is used to represent conditions that can be either true or false. Here's an example:

```
bool isReady = true;
```

## Integer

The int and uint types in Solidity are used to represent signed and unsigned integers, respectively. The size of the integer can vary depending on the number of bits used to represent it. Here are some examples:

```
int8 myInt8 = -10; 
uint256 myUint256 = 1000;
```

## Address

The address type in Solidity is used to represent Ethereum addresses. An Ethereum address is a 20-byte value that represents an account on the Ethereum blockchain. Here's an example:

```
address myAddress = 0x1234567890123456789012345678901234567890;
```

## Bytes

The bytes type in Solidity is used to represent a dynamic array of bytes. The byte type is used to represent a single byte. Here are some examples:

```
bytes memory myBytes = new bytes(10); 
byte myByte = 0x12;
```

## String

The string type in Solidity is used to represent a dynamic array of characters. Here's an example:

```
string memory myString = "Hello, World!";
```

## Arrays

Solidity supports both fixed-size and dynamic arrays. Here's an example of a fixed-size array:

```
uint256[3] myArray = [1, 2, 3];
```

And here's an example of a dynamic array:

```
uint256[] myDynamicArray;
```

## Structs

A struct is a custom data type that allows you to define a collection of variables with different data types. Here's an example:

```solidity
struct Person { 
    string name; 
    uint256 age; 
} 
Person myPerson = Person("Alice", 25);
```

## Enumerations

An enumeration is a custom data type that allows you to define a set of named values. Here's an example:

```solidity
enum Color {
    Red, 
    Green, 
    Blue
} 
Color myColor = Color.Red;
```

***

_That's it for the second lesson! In the next lesson, we'll cover functions in Solidity._
