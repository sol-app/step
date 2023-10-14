# Tips: Reentrancy

### Reentrancy

**Reentrancy** is a type of vulnerability that occurs when a contract calls an external contract, and then the external contract calls the first contract again before the first contract has finished executing. This can lead to unexpected behavior, such as an infinite loop, or the transfer of funds.

* **Example 1** In this example, we have a contract called Wallet that stores funds and can be used to make payments.

```solidity
contract Wallet {  
  address public owner;  
  mapping (address => uint) public balances; 

  constructor() public {    
    owner = msg.sender;  
  } 

  function deposit() public payable {    
    balances[msg.sender] += msg.value;  
  } 

  function withdraw(uint amount) public {    
    require(balances[msg.sender] >= amount);    
    msg.sender.transfer(amount);    
    balances[msg.sender] -= amount;  
  } 

  function pay(address payable _to, uint amount) public {    
    require(balances[msg.sender] >= amount);    
    _to.transfer(amount);    
    balances[msg.sender] -= amount;  
  }
}
```

The vulnerability arises when we use the pay function to call an external contract, and that external contract calls the Wallet contract again before the pay function is finished executing.

* **Example 2** In this example, we have a contract called Voting that stores votes and can be used to tally the results.

```solidity
contract Voting {  
  mapping (address => uint) public votes; 

  function castVote(uint _vote) public {    
    votes[msg.sender] = _vote;  
  } 

  function tallyResults() public {    
    uint result = 0;    
    for (uint i = 0; i < votes.length; i++) {      
      result += votes[i];    
      }    
    return result;  
  }
}
```

The vulnerability arises when we use the tallyResults function to call an external contract, and that external contract calls the Voting contract again before the tallyResults function is finished executing. This could lead to unexpected results, such as an incorrect tally of the votes.

#### Mitigation

In order to mitigate the risks associated with reentrancy, it is important to ensure that the contract checks for a sufficient amount of gas before making any external calls. Additionally, it is important to use the transfer function instead of the call function when making external calls. Finally, it is important to add a check to the contract to ensure that it is not called from the same address more than once.

***

### Detecting Reentrancy

Solidity provides the `require()` function, which can be used to detect reentrancy. require() checks a given boolean expression before running a function. For example, if a malicious user is able to call a vulnerable contract multiple times, require() can be used to detect this condition.

```solidity
contract ReentrancyHunter {  
  bool reentrancyDetected = false; 
  function vulnerableFunction(){    
    require(!reentrancyDetected);    
    // rest of vulnerableFunction code here    
    reentrancyDetected = true;  
  }
}
```

In the example above, the require() function checks the boolean variable reentrancyDetected before executing the `vulnerableFunction()` code. If reentrancyDetected is true, the require() statement will fail and the `vulnerableFunction()` code will not be executed.

### Preventing Reentrancy

Solidity also provides the `require()` function, which can be used to prevent reentrancy. require() checks a given boolean expression before running a function. For example, if a malicious user is able to call a vulnerable contract multiple times, require() can be used to detect this condition.

```solidity
contract ReentrancyHunter {  
  bool reentrancyPrevented = false; 
  function vulnerableFunction(){    
    require(!reentrancyPrevented);    
    // rest of vulnerableFunction code here    
    reentrancyPrevented = true;  
  }
}
```

In the example above, the require() function checks the boolean variable reentrancyPrevented before executing the `vulnerableFunction()` code. If reentrancyPrevented is false, the require() statement will succeed and the `vulnerableFunction()` code will be executed. Once the code has been executed, the reentrancyPrevented variable will be set to true, preventing the function from being executed again.

***

### Reentrancy Hack

* **Example 1** The following shows a vulnerable contract which can be exploited through reentrancy attack.

```solidity
contract Reentrancy {    
  uint public funds; 
  function depositFunds() payable public {        
    funds += msg.value;    
  } 
  
  function withdrawFunds() public {        
    if (funds > 0) {            
      uint amountToWithdraw = funds;            
      funds -= amountToWithdraw;            
      msg.sender.transfer(amountToWithdraw);        
    }    
  }
}
```

In the above example, the attacker can deposit some funds and then call the withdrawFunds function. Before the function completes, the attacker can call the depositFunds function again and then withdraw the funds again. This process can be repeated until all the funds are drained from the contract.

* **Example 2** The following is an example of a contract which is protected from reentrancy attack.

```solidity
contract Reentrancy {    
  uint public funds;    
  bool public fundsAreBeingWithdrawn; 
  
  function depositFunds() payable public {        
    funds += msg.value;    
  } 

  function withdrawFunds() public {        
    if (funds > 0 && !fundsAreBeingWithdrawn) {            
      fundsAreBeingWithdrawn = true;            
      uint amountToWithdraw = funds;            
      funds -= amountToWithdraw;            
      msg.sender.transfer(amountToWithdraw);            
      fundsAreBeingWithdrawn = false;        
    }    
  }
}
```

In the above example, the fundsAreBeingWithdrawn boolean flag is used to check if the withdrawFunds function is already in progress. If it is, the withdrawFunds function will not be called again. This prevents the attacker from repeatedly calling the depositFunds and withdrawFunds functions and draining the funds from the contract.
