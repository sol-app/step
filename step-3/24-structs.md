# 24: Structs

### Structs

Structs are custom data types that allow developers to define the data that they would like to store. They are typically used to store data that is related to one another, such as a user profile, a product, or a transaction record. Structs provide a convenient way to organize and access related information.

* User Profile

```solidity
struct Profile {    
    string name;    
    string email;    
    uint age;    
    string address;
}
```

The above code defines a Profile struct which contains 4 fields: name, email, age, and address.

* Product

```solidity
struct Product {    
    string name;    
    uint price;    
    uint quantity;    
    string description;
}
```

The above code defines a Product struct which contains 4 fields: name, price, quantity, and description.

* Transaction Record

```solidity
struct TransactionRecord {    
    address sender;    
    address recipient;    
    uint amount;    
    uint timestamp;
}
```

The above code defines a TransactionRecord struct which contains 4 fields: sender, recipient, amount, and timestamp.

***

### Import Structs

Structs are a powerful tool in Solidity, allowing you to create complex data structures. In this article, we'll look at how to use Import Structs to create better, more maintainable smart contract code.

* Why Use Import Structs? Importing Structs can help make your smart contracts more maintainable and reusable. By importing Structs, you can define a structure once and then use it in multiple contracts. This helps you keep your code DRY (Don't Repeat Yourself).
* How to Use Import Structs Using Import Structs is quite straightforward. All you need to do is define a Struct in a separate file and then import it into your smart contract.

Let's look at an example.

* Example Let's say you have a smart contract for an auction. In the auction smart contract, you want to store the details of each bidder. This will include their name, address, and bid amount.

To do this, you can define a Struct in a separate file like this:

```solidity
contract Bid { 
    struct Bidder {    
        string name;    
        address addr;    
        uint256 bidAmount;
    }
}
```

Then, in the auction smart contract, you can import the Struct and use it to store the bidder details like this:

```solidity
import "./Bid.sol"; 
contract Auction {    
    Bidder[] bidders; 
    function addBidder(string memory _name, address _addr, uint256 _bidAmount) public {        
        bidders.push(Bidder(_name, _addr, _bidAmount));    
    }
}
```

### Conclusion

Import Structs can help you make your smart contracts more maintainable and reusable. By defining Structs in separate files and then importing them into your smart contracts, you can keep your code DRY and more organized.

_That's it for the lesson 24! In the next lesson, Data Location_
