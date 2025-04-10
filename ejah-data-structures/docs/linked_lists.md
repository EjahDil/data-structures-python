# `SinglyLinkedList` Class Documentation

## Overview

The `SinglyLinkedList` class implements a singly linked list, a linear data structure where each element (node) points to the next element in the list. This class supports basic linked list operations such as insertion, deletion, searching, and traversal.


## Methods

### `__init__(self)`
Initializes the singly linked list with an empty list (`head` is set to `None`).

- **No parameters.**
- **Returns:** None

### `insert(self, data)`
Inserts a new node with the given data at the end of the list.

- **Parameters:**
  - `data` (any type): The value to be stored in the new node.
- **Returns:** None

- **Example:**

```python
linked_list = SinglyLinkedList()
linked_list.insert(5)
linked_list.insert(15)
print(linked_list.traverse())  # Output: [5, 15]
```

### `delete(self, data)`
Deletes the first occurrence of the node with the specified data.

- **Parameters:**
  - `data` (any type): The value of the node to be deleted.
- **Returns:** 
  - `True` if the node was found and deleted.
  - `False` if no node with the specified data was found.
  
- **Example:**

```python
linked_list = SinglyLinkedList()
linked_list.insert(5)
linked_list.insert(15)
linked_list.delete(5)
print(linked_list.traverse())  # Output: [15]
```

### `search(self, data)`
Searches for a node with the given data.

- **Parameters:**
  - `data` (any type): The value of the node to search for.
- **Returns:** 
  - `True` if a node with the specified data is found.
  - `False` if no node with the specified data is found.

- **Example:**

```python
linked_list = SinglyLinkedList()
linked_list.insert(10)
linked_list.insert(20)
print(linked_list.search(10))  # Output: True
print(linked_list.search(30))  # Output: False
```

### `traverse(self)`
Returns a list of all node data in the linked list from head to tail.

- **Returns:** A list of the node data in the order they appear in the list.

- **Example:**

```python
linked_list = SinglyLinkedList()
linked_list.insert(7)
linked_list.insert(14)
print(linked_list.traverse())  # Output: [7, 14]
```

### `__str__(self)`
Returns a string representation of the linked list, showing each node's data in a human-readable format.

- **Returns:** A string representing the linked list. If the list is empty, it returns `"Empty"`.

- **Example:**

```python
linked_list = SinglyLinkedList()
linked_list.insert(5)
linked_list.insert(12)
print(str(linked_list))  # Output: "5 -> 12"
linked_list.delete(5)
print(str(linked_list))  # Output: "12"
```

## Example Usage

#### Example Usage of `SinglyLinkedList` Class

```python
# Create a new SinglyLinkedList
linked_list = SinglyLinkedList()

# Insert elements
linked_list.insert(7)
linked_list.insert(14)
linked_list.insert(21)

# Traverse the list
print(linked_list.traverse())  # Output: [7, 14, 21]

# Search for an element
print(linked_list.search(14))  # Output: True
print(linked_list.search(28))  # Output: False

# Delete an element
linked_list.delete(14)
print(linked_list.traverse())  # Output: [7, 21]

```