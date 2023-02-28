# Tips: Remix Tutorial

### Remix Tutorial

This tutorial will provide an introduction to the **Remix development environment**, and show you how to use it to build simple smart contracts.

* Setting Up To get started, open the Remix development environment at [remix.ethereum.org](https://remix.ethereum.org/).
* Writing The Contract We'll write a simple smart contract that stores an integer. To do this, create a new file in the Remix editor and name it `MyContract.sol`. Then copy-paste the following code into it:

```solidity
pragma solidity ^0.8; 
contract MyContract {  
    int myInteger;  
      
    constructor() public {    myInteger = 0;  }   
     
    function setInteger(int _myInteger) public {    
        myInteger = _myInteger;  
    }    
    
    function getInteger() public view returns (int) {
        return myInteger;  
    }
}
```

* Compiling The Contract Next, we need to compile the contract. To do this, click the "Compile" tab on the left-hand side and select MyContract.sol from the dropdown. Remix will compile the contract, and you should see a "Success" message in the compile output.
* Deploying The Contract Now that the contract is compiled, we can deploy it to the Ethereum network. To do this, click the "Run" tab on the left-hand side. Remix will open a new window that allows you to deploy the contract.

Fill in the form with the following details:

* Environment: Injected Web3
* Account: Select the account you want to use
* Gas limit: Leave this as the default Then click the "Deploy" button. Remix will deploy the contract to the Ethereum network, and you should see a "Success" message in the deploy output.
* Interacting With The Contract Now that the contract is deployed, we can interact with it. To do this, we need to first get the contract's address. This is displayed in the deploy output.

Copy the contract address and then go back to the "Run" tab. Paste the address into the "At Address" field and click the "At Address" button. This will open a new window that allows you to interact with the contract.

Now you can call the functions of the contract, for example, the getInteger function. To do this, click the "getInteger" button, and you should see the value of the myInteger variable in the function output.

You can also set the value of the myInteger variable by calling the setInteger function and passing in a new value. To do this, click the "setInteger" button, enter a new value, and then click the "Submit" button. You should see a "Success" message in the function output.

### Conclusion

Congratulations, you have successfully created and deployed your first smart contract using Remix!
