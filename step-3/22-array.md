# 22: Array

### Array

An Array is a data structure that can be used to store a collection of data elements. In Solidity, an array can be of any data type, including structs, mappings, and other arrays.

Here are some examples of arrays in Solidity:

* **Example 1**:

```solidity
uint[4] array;
```

This is an array of type uint of size 4.

* **Example 2**:

```solidity
struct User {    
    string name;    
    uint age;
} 
User[2] users;
```

This is an array of type User of size 2.

* **Example 3**:

```solidity
mapping (uint => uint) mappingA;
uint[] arrayOfMappingsA; // arrayOfMappingsA[i] = x;

// complex array = matrix => actually we dont use in projects~
uint[][] arrayOfMappingsB; 
```

***

### Dynamic Arrays

A dynamic array is a data structure that can store a variable number of elements. It can be used to store a list of elements that can grow and shrink as needed. Here are some examples of dynamic arrays in Solidity:

* **Example 1**: Using push() The push() function can be used to add elements to a dynamic array.

```solidity
contract Example1 {    
    uint[] arr; 
    function addElement(uint element) public {        
        arr.push(element);    
    }
}
```

* **Example 2**: Using length The length property can be used to get the length of a dynamic array.

```solidity
contract Example2 {    
    uint[] arr; 
    function getLength() public view returns (uint) {        
        return arr.length;    
    }
}
```

* **Example 3**: Using delete The delete keyword can be used to delete elements from a dynamic array.

```solidity
contract Example3 {    
    uint[] arr; 
    function deleteElement(uint element) public {        
        delete arr[element];    
    }
}
```

***

### Replace Array

This article looks at how to replace an array in Solidity using some examples.

* **Example 1** Let's say we have an array like this:

```solidity
uint[] numbers = [1, 2, 3, 4, 5];
```

We can replace this array with a new one, like this:

```solidity
uint[] newNumbers = [6, 7, 8, 9, 10];
numbers = newNumbers;
```

* **Example 2** Let's say we have an array like this:

```solidity
string[] names = ["Alice", "Bob", "Carol"];
```

We can replace this array with a new one, like this:

```solidity
string[] newNames = ["Dave", "Eve", "Frank"];
names = newNames;
```

* **Example 3** Let's say we have an array like this:

```solidity
bytes32[] hashes = [hash1, hash2, hash3];
```

We can replace this array with a new one, like this:

```solidity
bytes32[] newHashes = [hash4, hash5, hash6];
hashes = newHashes;
```

***

### Array Remove

Removing elements from an array can be done in Solidity with the array.remove() function. This function takes a single argument, the element to be removed, and removes it from the array.

* **Example 1**

```solidity
uint[] array = [1, 2, 3, 4, 5];
array.remove(2);
```

After calling remove(2), the array now contains \[1, 3, 4, 5].

* **Example 2**

```solidity
string[] array = ["Alice", "Bob", "Charlie", "David"];
array.remove("Charlie");
```

After calling remove("Charlie"), the array now contains \["Alice", "Bob", "David"].

***

### Array Pop

Array pop is a useful function in Solidity that removes the last element from an array and returns it. This function is important for managing memory and working with dynamic arrays.

* **Example 1** We can use array pop to remove the last element from an array and store it in a variable.

```solidity
uint[] myArray = [1, 2, 3, 4];
uint lastElement = myArray.pop();
```

In this example, the variable lastElement will have the value 4 and the array myArray will have the values \[1, 2, 3].

* **Example 2** We can also use array pop to remove elements from the end of a dynamic array.

```solidity
uint[] memory dynamicArray = new uint[](3);
dynamicArray[0] = 4;
dynamicArray[1] = 7;
dynamicArray[2] = 9;
uint lastElement = dynamicArray.pop();
```

In this example, the variable lastElement will have the value 9 and the array dynamicArray will have the values \[4, 7].

***

### Array Methods - by Some Examples

Solidity provides numerous array methods that allow you to manipulate array values in a variety of ways. Here are some examples of how you can use array methods to work with arrays of data.

* `push()` The `push()` method adds an element to the end of an array.

```solidity
contract ArrayExample {    
    string[] public arrayData; 
    // add a string to the end of the array    
    function pushArray(string memory _value) public {        
        arrayData.push(_value);    
    }
}
```

* `length()` The length() method returns the length (number of elements) in an array.

```solidity
contract ArrayExample {    
    string[] public arrayData; 
    // returns the length of the array    
    function getLength() public view returns (uint) {        
        return arrayData.length;    
    }
}
```

* `pop()` The pop() method removes the last element from an array.

```solidity
contract ArrayExample {    
    string[] public arrayData; 
    // remove the last element from the array    
    function popArray() public {        
        arrayData.pop();    
    }
}
```

* `slice()` The slice() method returns a shallow copy of a portion of an array into a new array object.

<pre class="language-solidity"><code class="lang-solidity">contract ArrayExample {    
    string[] public arrayData; 
    // returns a shallow copy of a portion of an array    
    function getSlice(uint start, uint end) public view returns (string[] memory) {        
        return arrayData.slice(start, end);    
<strong>    }
</strong>}
</code></pre>

These are just a few of the array methods available in Solidity. For a full list of array methods, see [the Solidity documentation](https://solidity.readthedocs.io/en/v0.8.0/types.html#arrays).

{% hint style="info" %}
Some of these methods not included yet in solidity
{% endhint %}

_That's it for the lesson 22! In the next lesson, Enum_
