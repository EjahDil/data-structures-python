# `BinarySearchTree` Class Documentation

## Overview

The `BinarySearchTree` class implements a binary search tree data structure. A binary search tree is a tree where each node has at most two children, and the left child is smaller than the parent node, while the right child is larger. This class provides methods for inserting, searching, and performing inorder traversal of the tree.

## Attributes

- `root`: The root node of the binary search tree. Initially set to `None`.

## Methods

### `__init__(self)`
Initializes an empty binary search tree.

- **Parameters:** None
- **Returns:** None

### `insert(self, data)`
Inserts a new node with the given data into the binary search tree. It places the node at the correct position based on BST properties (left for smaller values, right for larger values).

- **Parameters:**
  - `data` (any type): The data to be inserted into the tree.
- **Returns:** None

- **Example:**

```python
bst = BinarySearchTree()
bst.insert(10)
bst.insert(5)
bst.insert(15)
print(bst)  # Output: 5 -> 10 -> 15
```

### `search(self, data)`
Searches for a node with the given data in the binary search tree.

- **Parameters:**
  - `data` (any type): The data to search for in the tree.
- **Returns:**
  - `True`: If the data is found in the tree.
  - `False`: If the data is not found.
  
- **Example:**

```python
bst = BinarySearchTree()
bst.insert(10)
bst.insert(5)
bst.insert(15)
print(bst.search(10))  # Output: True
print(bst.search(20))  # Output: False
```

### `_insert_recursive(self, node, data)`
Helper function (often prefixed with an underscore to indicate it’s meant for internal use) to recursively insert a new node into the tree.

- **Parameters:**
  - `node`: The current node being examined for insertion.
  - `data` (any type): The data to be inserted.
- **Returns:** None (Recursive insertion)

### `_search_recursive(self, node, data)`
Helper function (often prefixed with an underscore to indicate it’s meant for internal use) to recursively search for a node with the given data.

- **Parameters:**
  - `node`: The current node being examined.
  - `data` (any type): The data to search for.
- **Returns:**
  - `True`: If the data is found in the tree.
  - `False`: If the data is not found.

### `_inorder_recursive(self, node, elements)`
Helper function (often prefixed with an underscore to indicate it’s meant for internal use) for performing an inorder traversal of the tree.

- **Parameters:**
  - `node`: The current node being examined during traversal.
  - `elements` (list): A list to store the nodes during traversal.
- **Returns:** None (Recursive traversal)

### `inorder_traversal(self)`
Returns a list of the elements in the binary search tree in inorder (left, root, right).

- **Returns:** 
  - A list of elements in the tree sorted in ascending order.

- **Example:**

```python
bst = BinarySearchTree()
bst.insert(10)
bst.insert(5)
bst.insert(15)
print(bst.inorder_traversal())  # Output: [5, 10, 15]
```

### `__str__(self)`
Returns a string representation of the binary search tree by performing an inorder traversal.

- **Returns:** A string in the format `value1 -> value2 -> ...` for the elements in the tree.

  - If the tree is empty, it returns `"Empty"`.

- **Example:**

```python
bst = BinarySearchTree()
bst.insert(4)
bst.insert(2)
bst.insert(6)
print(str(bst))  # Output: "2 -> 4 -> 6"
```

## Example Usage

#### Example Usage of `Binary ` Class

```python
# Create a new Binary Search Tree
bst = BinarySearchTree()

# Insert elements into the BST
bst.insert(30)
bst.insert(20)
bst.insert(40)
bst.insert(10)
bst.insert(25)

# Print the BST (Inorder Traversal)
print(bst)  # Output: 10 -> 20 -> 25 -> 30 -> 40

# Search for an element in the BST
print(bst.search(25))  # Output: True
print(bst.search(50))  # Output: False

# Get the elements in Inorder Traversal
print(bst.inorder_traversal())  # Output: [10, 20, 25, 30, 40]

```