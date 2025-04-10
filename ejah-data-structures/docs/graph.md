# `BinaryGraphSearch` Class Documentation

## Overview
The `BinaryGraphSearch` class implements binary search operations on a sorted list. It provides methods to search for a target element, insert a value while maintaining the order of the list, and traverse the list in order.

## Methods

### `__init__(self, data)`
This method initializes the `BinaryGraphSearch` instance with a sorted list.

**Parameters:**
- `data` (list): A list of elements that must be sorted in non-decreasing order.

**Raises:**
- `ValueError`: If the input list is not sorted in non-decreasing order.

**Example:**
```python
graph = BinaryGraphSearch([1, 2, 3, 4, 5])  # Valid sorted list
```

### `_binary_search(self, data, target)`
This is a helper function that performs a recursive binary search on a given sorted list.

**Parameters:**
- `data` (list): The sorted list to search.
- `target` (any): The value to search for in the list.

**Returns:**
- `int`: The index of the target element in the list if found, otherwise `-1`.

**Example:**
```
graph._binary_search([1, 2, 3, 4, 5], 3)  # Returns 2
```

### `search(self, target)`
This method searches for a target element in the sorted list using binary search.

**Parameters:**
- `target` (any): The value to search for in the list.

**Returns:**
- `int`: The index of the target element if found, otherwise `-1`.

**Example:**
```python
graph = BinaryGraphSearch([1, 2, 3, 4, 5])
print(graph.search(3))  # Returns 2
print(graph.search(6))  # Returns -1
```

### `insert(self, value)`
This method inserts a value into the sorted list, maintaining the order.

**Parameters:**
- `value` (any): The value to insert into the list.

**Example:**
```python
graph = BinaryGraphSearch([1, 2, 3, 5])
graph.insert(4)  # Inserts 4 maintaining the order
print(graph)  # Output: Sorted List: [1, 2, 3, 4, 5]
```

### `inorder_traversal(self)`
This method returns the sorted list, simulating an in-order traversal.

**Returns:**
- `list`: The sorted list of elements.

**Example:**
```python
graph = BinaryGraphSearch([1, 2, 3, 4, 5])
print(graph.inorder_traversal())  # Returns [1, 2, 3, 4, 5]
```

### `__str__(self)`
This method provides a string representation of the object.

**Returns:**
- `str`: A string representation of the sorted list in the format "Sorted List: [elements]".

**Example:**
```python
graph = BinaryGraphSearch([1, 2, 3, 4, 5])
print(graph)  # Output: Sorted List: [1, 2, 3, 4, 5]
```

## Example

#### Example Usage of `BinaryGraphSearch` Class

```python
# Create an instance of BinaryGraphSearch with a sorted list
graph = BinaryGraphSearch([1, 2, 3, 4, 5])

# Search for an element
print(graph.search(2))  # Output: 2
print(graph.search(8))  # Output: -1

# Insert a new element while maintaining the order
graph.insert(4)  # Does not change the list
print(graph)  # Output: Sorted List: [1, 2, 3, 4, 5]
```