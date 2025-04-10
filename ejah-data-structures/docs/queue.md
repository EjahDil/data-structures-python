# `Queue` Class Documentation

## Overview

The `Queue` class implements a queue data structure using a list. A queue follows the FIFO (First-In-First-Out) principle, where elements are added at the end (enqueue) and removed from the front (dequeue). This class provides basic queue operations such as enqueue, dequeue, peek, and checks if the queue is empty.


## Methods

### `__init__(self)`
Initializes an empty queue using a list.

- **Parameters:** None
- **Returns:** None

### `enqueue(self, item)`
Adds an item to the end of the queue.

- **Parameters:**
  - `item` (any type): The element to be added to the queue.
- **Returns:** None

- **Example:**

```python
queue = Queue()
queue.enqueue(5)
queue.enqueue(15)
print(queue)  # Output: Queue([5, 15])
```

### `dequeue(self)`
Removes and returns the front item from the queue.

- **Returns:** The front item of the queue.
- **Raises:**
  - `IndexError`: If the queue is empty.

- **Example:**

```python
queue = Queue()
queue.enqueue(30)
queue.enqueue(40)
print(queue.dequeue())  # Output: 30
print(queue)  # Output: Queue([40])
```

### `peek(self)`
Returns the front item without removing it.

- **Returns:** The front item of the queue.
- **Raises:**
  - `IndexError`: If the queue is empty.

- **Example:**

```python
queue = Queue()
queue.enqueue(10)
queue.enqueue(20)
print(queue.peek())  # Output: 10
```

### `is_empty(self)`
Checks if the queue is empty.

- **Returns:** 
  - `True`: If the queue is empty.
  - `False`: If the queue contains at least one item.

- **Example:**

```python
queue = Queue()
print(queue.is_empty())  # Output: True
queue.enqueue(18)
print(queue.is_empty())  # Output: False
```

### `__str__(self)`
Returns a string representation of the queue.

- **Returns:** A string in the format `Queue([item1, item2, item3, ...])`.

- **Example:**

```python
queue = Queue()
queue.enqueue(16)
queue.enqueue(20)
print(str(queue))  # Output: "Queue([16, 20])"
```

## Example Usage

#### Example Usage of `Queue` Class

```python
# Create a new Queue
queue = Queue()

# Enqueue elements
queue.enqueue(50)
queue.enqueue(60)
queue.enqueue(70)

# Print the queue
print(queue)  # Output: Queue([50, 60, 70])

# Peek at the front item
print(queue.peek())  # Output: 50

# Dequeue an item
print(queue.dequeue())  # Output: 50

# Print the updated queue
print(queue)  # Output: Queue([60, 70])

# Check if the queue is empty
print(queue.is_empty())  # Output: False

# Dequeue the remaining items
queue.dequeue()
queue.dequeue()

# Check if the queue is empty again
print(queue.is_empty())  # Output: True
```