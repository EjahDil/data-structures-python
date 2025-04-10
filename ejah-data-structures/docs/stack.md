# `Stack` Class Documentation

## Overview

The `Stack` class implements a stack data structure using a list. A stack follows the LIFO (Last-In-First-Out) principle, where elements are added to the top (push) and removed from the top (pop). This class provides basic stack operations such as push, pop, peek, and checks if the stack is empty.


## Methods

### `__init__(self)`
Initializes an empty stack using a list.

- **Parameters:** None
- **Returns:** None

### `push(self, item)`
Adds an item to the top of the stack.

- **Parameters:**
  - `item` (any type): The element to be added to the stack.
- **Returns:** None

- **Example:**

```python
stack = Stack()
stack.push(30)
stack.push(40)
print(stack)  # Output: Stack([30, 40])
```

### `pop(self)`
Removes and returns the top item from the stack.

- **Returns:** The top item of the stack.
- **Raises:**
  - `IndexError`: If the stack is empty.

- **Example:**

```python
stack = Stack()
stack.push(50)
stack.push(60)
print(stack.pop())  # Output: 60
print(stack)  # Output: Stack([50])
```

### `peek(self)`
Returns the top item without removing it.

- **Returns:** The top item of the stack.
- **Raises:**
  - `IndexError`: If the stack is empty.

- **Example:**

```python
stack = Stack()
stack.push(30)
stack.push(40)
print(stack.peek())  # Output: 40
```

### `is_empty(self)`
Checks if the stack is empty.

- **Returns:**
  - `True`: If the stack is empty.
  - `False`: If the stack contains at least one item.

- **Example:**

```python
stack = Stack()
print(stack.is_empty())  # Output: True
stack.push(13)
print(stack.is_empty())  # Output: False
```

### `__str__(self)`
Returns a string representation of the stack.

- **Returns:** A string in the format `Stack([item1, item2, item3, ...])`.

- **Example:**

```python
stack = Stack()
stack.push(14)
stack.push(18)
print(str(stack))  # Output: "Stack([14, 18])"
```

## Example Usage

#### Example Usage of `Stack` Class

```python
# Create a new Stack
stack = Stack()

# Push elements onto the stack
stack.push(50)
stack.push(60)
stack.push(70)

# Print the stack
print(stack)  # Output: Stack([50, 60, 70])

# Peek at the top item
print(stack.peek())  # Output: 70

# Pop an item
print(stack.pop())  # Output: 70

# Print the updated stack
print(stack)  # Output: Stack([50, 60])

# Check if the stack is empty
print(stack.is_empty())  # Output: False

# Pop the remaining items
stack.pop()
stack.pop()

# Check if the stack is empty again
print(stack.is_empty())  # Output: True
```