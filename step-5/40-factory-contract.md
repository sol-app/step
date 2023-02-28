# 40: Factory Contract

A factory contract is a type of smart contract used to create and deploy other smart contracts. It is used to maintain a registry of deployed contracts, as well as to provide a convenient way to access and interact with them.\
_"A Factory Contract is a type of smart contract that allows for the deployment of multiple smart contracts from a single code base. This can be useful for developers that want to deploy many contracts with the same functionality without having to write and deploy each one separately."_

* Example: ERC721 Token Factory In this example, we will be creating a factory contract to create ERC721 tokens. First, we need to define the contract interface:

```solidity
contract ERC721TokenFactory {    
    // Events    
    event TokenCreated(
        address indexed addressOfToken, string name, string symbol
    ); 
    
    // Functions    
    function createERC721(string memory name, string memory symbol) 
    public returns (address contractAddress) {        
        // Create a new ERC721 contract        
        // and emit a TokenCreated event    
    } 

    function getERC721(address tokenAddress) 
    public view returns (string memory name, string memory symbol) {   
        // Get the name and symbol of an existing ERC721 contract    
    }
}
```

Now, we can implement the contract. We can start with the createERC721 function:

```solidity
function createERC721(string memory name, string memory symbol) 
public returns (address contractAddress) {    
    // Create a new ERC721 contract    
    ERC721 token = new ERC721(name, symbol); 
    // Emit a TokenCreated event    
    emit TokenCreated(address(token), name, symbol); 
    // Return the address of the newly created contract   
     return address(token);
}
```

And finally, we can implement the getERC721 function:

```solidity
function getERC721(address tokenAddress) 
public view returns (string memory name, string memory symbol) {    
    // Get a reference to the ERC721 contract    
    ERC721 token = ERC721(tokenAddress); 
    // Return the name and symbol of the contract    
    return (token.name(), token.symbol());
}
```

With this factory contract in place, we can now easily create and access ERC721 token contracts.

***

**To illustrate this concept, let's look at an example**:

* Example Say we want to create a simple factory contract that deploys a new ERC20 token for each customer. We can write a single Factory contract to handle all customer requests. Here's an example of how it could look:

```solidity
contract Factory {    
    uint public tokenCount;        
    constructor() public {        tokenCount = 0;    }        
    function createToken() public returns (uint) {        
        tokenCount++;        
        // Create and deploy the new token contract        
        uint tokenId = createERC20(tokenCount);        
        return tokenId;    
    }        
    // Function to create and deploy the new ERC20 token    
    function createERC20(uint tokenId) private returns (uint) {        
        // Create and deploy the new ERC20 token contract        
        // Pass the tokenId as an argument        
        ERC20 token = new ERC20(tokenId);        
        // Return the tokenId        
        return tokenId;    
    }
}
```

In this example, the Factory contract is responsible for creating a new ERC20 token and returning the tokenId of the newly created token. The tokenId is used to identify the token contract. The Factory contract can be called multiple times to create multiple ERC20 tokens.

* Benefits Factory Contracts have several benefits over creating each contract separately. For example, it can reduce the amount of code and deployment time needed for multiple smart contracts with similar functionality. It can also be easier to manage and track all contracts spawned from the Factory contract. Additionally, Factory Contracts can be used to create more complex contracts with more features that require multiple contracts to build.

_That's it for the lesson 40! In the next lesson, Proxy Contract_
