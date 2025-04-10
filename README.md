# Ejah Data Structures Python Package

Ejah Data Structures is a Python package that provides various data structures with common operations such as insert, delete, search, and traverse. This package includes implementations of the following data structures: Array, Binary Search Tree, Binary Graph Search, Singly Linked List, Queue, and Stack.

## Installation

To install the Ejah Data Structures Python package, ensure you have Python installed on your system. You can install the package using `pip`:

```bash
pip install ejah-data-structures
```

Make sure you run this command within a Python environment.

## Features

This package includes the following data structures, each with its own module containing methods for insert, delete, search, traverse, and more:

### Array

The `Array` class provides a dynamic array implementation with operations to insert, delete, search, and traverse the array.

#### Methods

- **Insert(index, value)**: Adds an element at a specified index.
- **Delete(index)**: Removes an element from a given index.
- **Search(value)**: Searches for an element and returns its index.
- **Traverse()**: Returns all elements in the array.
- **Length()**: Returns the number of elements in the array.
- **Is Empty()**: Checks if the array is empty.


<!-- # Example usage:

array = Array()
array.insert(0, 10)
print(array.search(10))  # Output: 0
Read the detailed Array documentation here -->

### Binary Graph Search

The `BinaryGraphSearch` class allows for binary search on a sorted list of data. This class implements both the search operation and the insert operation to maintain the list in sorted order.

#### Methods

- **Search(target)**: Searches for a target element using binary search.
- **Insert(value)**: Inserts a value into the list while maintaining the sorted order.
- **In-order Traversal()**: Simulates an in-order traversal of the binary tree (which is essentially the sorted list).

### Binary Search Tree

The `BinarySearchTree` class implements a binary search tree, which allows for efficient searching, insertion, and traversal of nodes in sorted order.

#### Methods

- **Insert(data)**: Inserts a node with the given data.
- **Search(data)**: Searches for a node with the specified data.
- **In-order Traversal()**: Returns the nodes in sorted order (in-order traversal).


### Singly Linked List

The `SinglyLinkedList` class provides a basic singly linked list implementation.

#### Methods

- **Insert(data)**: Adds a new node at the end of the list.
- **Delete(data)**: Removes a node with the specified value.
- **Search(data)**: Searches for a node containing a specific value.
- **Traverse()**: Returns a list of all nodes' data.

### Queue

The `Queue` class implements a FIFO (First-In-First-Out) structure, which is useful for scenarios like task scheduling.

#### Methods

- **Enqueue(item)**: Adds an item to the end of the queue.
- **Dequeue()**: Removes and returns the front item from the queue.
- **Peek()**: Returns the front item without removing it.
- **Is Empty()**: Checks if the queue is empty.

### Stack

The `Stack` class implements a LIFO (Last-In-First-Out) structure, which is essential for undo operations, function calls, and parsing expressions.

#### Methods

- **Push(item)**: Adds an item to the top of the stack.
- **Pop()**: Removes and returns the top item from the stack.
- **Peek()**: Returns the top item without removing it.
- **Is Empty()**: Checks if the stack is empty.

Usage
After installation, you can start using the package by importing the classes directly into your Python code.

## Usage

After installation, you can start using the package by importing the classes directly into your Python code.

```python

from ejah_data_structures import Array, Queue, Stack, SinglyLinkedList, BinaryGraphSearch, BinarySearchTree

```

Contribute
If you'd like to contribute to this project, please visit the GitHub repository and submit issues, pull requests, or suggestions.

Feel free to fork the project and make improvements or add new features to enhance its usefulness.

License
This project is licensed under the MIT License - see the LICENSE file for details.