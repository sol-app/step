# 42: Create2

### Create2

Create2 is a new Ethereum smart contract creation method introduced in the Constantinople hard fork. It allows for off-chain contract deployment, which means that users can deploy a contract without broadcasting the transaction to the blockchain.

#### Advantages

Create2 offers several advantages for contract deployment:

**Faster Deployment**: Because it does not require broadcasting a transaction to the blockchain, contract deployment with Create2 can be completed in a fraction of the time it would take to deploy a contract on-chain.

**Flexibility**: Create2 allows users to deploy contracts that are tied to specific addresses, which makes it possible to deploy contracts to any address, even if the address does not exist on the blockchain.

**Security**: Create2 offers improved security by allowing users to deploy contracts to an address that is not known to anyone else. This means that malicious actors cannot target the contract before it is deployed.

#### Examples | Usecase

Here are some examples of how you can use Create2:

**Multi-Signature Wallets**: Create2 can be used to deploy multisig wallets that are tied to a specific address. This allows users to create wallets that are not tied to any existing address, making them more secure.

**Crowdfunding**: Create2 can be used to deploy crowdfunding smart contracts that are tied to specific addresses. This makes it possible to create crowdfunding campaigns that are not tied to any existing address, making them more secure.

**Decentralized Exchanges**: Create2 can be used to deploy decentralized exchanges that are tied to specific addresses. This makes it possible to create exchanges that are not tied to any existing address, making them more secure.

**Deploying a Proxy Contract**: With Create2, users can deploy a proxy contract to a known address before the contract code is deployed to the Ethereum network. This allows users to access the contract before it is deployed, such as when using a multisig wallet.

**Deploying a Contract Upgrade**: Create2 also allows users to deploy a contract upgrade without the need to redeploy the original contract. This can be done by setting the nonce to the same value as the nonce used for the original contract. This allows users to deploy an upgrade without having to redeploy the original contract.

**Deploying a Contract With Known Parameters**: Create2 also allows users to deploy a contract with known parameters. This allows users to deploy a contract with pre-defined parameters, such as the fee structure for a decentralized exchange. This can be done by setting the nonce to the same value as the nonce used for the original contract.

***

### Benefits of using create2

**Deployment security** - create2 allows for a deterministic address for a contract deployment, allowing developers to deploy contracts to a predictable address, improving security by avoiding the potential for malicious actors to deploy at the same address.

**Gas efficiency** - create2 allows for the deployment of contracts to pre-existing addresses, avoiding the need to use additional gas for deploying to a new address.

#### Example Code

The following Solidity code shows how to use create2 to deploy a contract to a pre-existing address:

```solidity
contract Deployer {    
    bytes4 public constant CREATE2_ID = 0xbb9bc244; 
    constructor() public {        
        // Address of contract to be deployed        
        bytes20 targetAddress = 0x12345678901234567890; 
        // Deploy the contract to the target address        
        address contractAddress = address(uint160(
        keccak256(abi.encodePacked(CREATE2_ID, this, targetAddress))
        ));        
        (new Foo()).deploy(contractAddress);    
    }
} 
contract Foo {    // Contract code    // ...}
```

**Further Reading**

* [EIP-1014: Skinny CREATE2](https://eips.ethereum.org/EIPS/eip-1014)
* [Solidity Documentation - CREATE2](https://solidity.readthedocs.io/en/v0.8.0/control-structures.html#create2)

> **Ethereum censored** my country. <mark style="color:blue;">search</mark>: <mark style="color:red;">**eip-1014**</mark> <mark style="color:blue;">for more detail</mark>

_That's it for the lesson 42! In the next lesson, Try Catch_
