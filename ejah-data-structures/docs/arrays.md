# `Array` Class Documentation

The `Array` class provides a simple implementation of an array-like data structure with basic operations such as insertion, deletion, searching, and traversal. Below is a breakdown of each method and the functionality of the class.

## Class Overview

The `Array` class simulates an array-like structure with the ability to perform the following operations:
- Insertion of values at specified indices.
- Deletion of values from specified indices.
- Searching for values within the array.
- Traversing the array to return all its elements.
- Checking the length of the array.
- Checking if the array is empty.
  
Internally, the class uses a list to store the elements.

## Methods

### `__init__(self)`
The constructor method initializes an empty list (`self.array`), which will be used to store elements in the array.

**Usage:**

```python
arr = Array()
```

### `insert(self, index, value)`
This method inserts a value at the specified index.

**Parameters:**

- `index` (int): The index at which the value should be inserted.
- `value` (any): The value to insert into the array.

**Error Handling:**
- If the `index` is out of bounds (either less than 0 or greater than the length of the array), it prints an error message: `"Error: Index out of bounds."`


**Example:**

```python
arr = Array()
arr.insert(2, 14)  # Inserts 14 at index 2
arr.insert(0, 30)  # Inserts 30 at index 0
```

### `delete(self, index)`
This method deletes the element at the specified index.

**Parameters:**
- `index` (int): The index of the element to delete.

**Error Handling:**
- If the `index` is out of bounds (less than 0 or greater than or equal to the length of the array), it prints an error message: `"Error: Index out of bounds."`

**Example:**
```python
arr = Array()
arr.insert(0, 14)
arr.insert(1, 30)
arr.delete(1)  # Deletes the element at index 1
```

### `search(self, value)`
This method searches for a value in the array and returns its index if found, or -1 if the value is not found.

**Parameters:**
- `value` (any): The value to search for.

**Returns:**
- The index of the value if it is found, otherwise -1.

**Example:**
```python
arr = Array()
arr.insert(0, 12)
arr.insert(1, 20)
arr.search(12)  # Returns 0
arr.search(25)  # Returns -1
```
### `traverse(self)`
This method returns all the elements in the array as a list.

**Returns:**
- The array (list of elements).

**Example:**
```python
arr = Array()
arr.insert(0, 20)
arr.insert(1, 5)
arr.traverse()  # Returns [20, 5]

```
### `length(self)`
This method returns the number of elements in the array.

**Returns:**
- The length (number of elements) of the array.

**Example:**
```python
arr = Array()
arr.insert(0, 40)
arr.length()  # Returns 1
```

### `is_empty(self)`
This method checks if the array is empty.

**Returns:**

- `True` if the array is empty.  
- `False` if the array contains any elements.

**Example:**
```python
arr = Array()
arr.is_empty()  # Returns True
arr.insert(0, 18)
arr.is_empty()  # Returns False
```

### `__str__(self)`
This method provides a string representation of the array for easy printing.

**Returns:**
- A string in the format: `"Array: [elements]"`

**Example:**
```python
arr = Array()
arr.insert(0, 10)
arr.insert(1, 20)
print(arr)  # Uses __str__ method
```
## Example

#### Example Usage of the `Array` Class

```python
# Create an instance of Array
arr = Array()

# Insert elements
arr.insert(0, 12)
arr.insert(1, 14)
arr.insert(2, 16)

# Traverse the array
print(arr.traverse())  # Output: [12, 14, 16]

# Search for a value
print(arr.search(12))  # Output: 1
print(arr.search(20))  # Output: -1

# Delete an element
arr.delete(1)  # Deletes the element at index 1 (12)
print(arr.traverse())  # Output: [14, 16]

# Check the length of the array
print(arr.length())  # Output: 2

# Check if the array is empty
print(arr.is_empty())  # Output: False
```
