# Tips: Solidity by "Immunable"

### Solidity by "Immunable"

Immunable is a framework for writing smart contracts in Solidity that makes them more secure and easier to work with. It provides a set of tools and best practices that make it easier to write secure and robust contracts.

Tools\
Immunable provides several tools to help developers write secure and robust smart contracts.

Contract Security Scanner\
The Contract Security Scanner is a tool that helps developers identify potential security issues in their contracts. It scans the source code and provides a set of recommendations for improving security.

Contract Security Library\
The Contract Security Library is a set of functions and best practices for making smart contracts secure. It includes functions for verifying inputs, managing permissions, and more.

Contract Security Checklist\
The Contract Security Checklist helps developers ensure that their contracts are secure. It includes a list of best practices that should be followed when writing smart contracts.

Examples\
Let's look at a few examples of Immunable in action.

Verifying Inputs\
The Contract Security Library includes a function for verifying inputs. This function takes a function argument and verifies that it is of the expected type.

```javascript
function verifyInput(input) {  
    require(typeof input == "string");
}
```

Managing Permissions\
The Contract Security Library also includes a function for managing permissions. This function takes a permission argument and verifies that the caller has the necessary permission to call the function.

```javascript
function managePermission(permission) {  
    require(msg.sender.caller.hasPermission(permission));
}
```

Validating Transactions\
The Contract Security Library also includes a function for validating transactions. This function takes a transaction argument and verifies that it is valid before executing the transaction.

```javascript
function validateTransaction(transaction) {  
    require(transaction.value >= 0);
}
```

### Conclusion

Immunable is a framework for writing secure and robust smart contracts in Solidity. It provides a set of tools and best practices that make it easier to write secure contracts. Examples of Immunable in action include verifying inputs, managing permissions, and validating transactions.
