# JS Data Structure Operators

This project showcases various data structure operations implemented in JavaScript. The focus is on demonstrating basic and advanced operations on common data structures like arrays, stacks, queues, and linked lists.

## Features

- Array operations (e.g., push, pop, shift, unshift)
- Stack implementation
- Queue implementation
- Linked List implementation

## Demo

Check out the live demo [here](https://qyuzet.github.io/js-data-structure-operators).

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/Qyuzet/js-data-structure-operators.git
    ```
2. Navigate to the project directory:
    ```sh
    cd js-data-structure-operators
    ```

## Usage

Open `index.html` in your preferred browser to view and interact with the data structure operations.

## JavaScript Snippet Explanation

### Array Operations
```javascript
let array = [1, 2, 3, 4, 5];

// Add an element to the end
array.push(6);

// Remove an element from the end
array.pop();

// Add an element to the beginning
array.unshift(0);

// Remove an element from the beginning
array.shift();
```
- Demonstrates basic array operations like `push`, `pop`, `unshift`, and `shift`.

### Stack Implementation
```javascript
class Stack {
  constructor() {
    this.items = [];
  }
  push(element) {
    this.items.push(element);
  }
  pop() {
    if (this.items.length == 0) return "Underflow";
    return this.items.pop();
  }
  peek() {
    return this.items[this.items.length - 1];
  }
}
```
- Shows a basic implementation of a stack with methods for `push`, `pop`, and `peek`.

### Queue Implementation
```javascript
class Queue {
  constructor() {
    this.items = [];
  }
  enqueue(element) {
    this.items.push(element);
  }
  dequeue() {
    if (this.items.length == 0) return "Underflow";
    return this.items.shift();
  }
  front() {
    return this.items[0];
  }
}
```
- Shows a basic implementation of a queue with methods for `enqueue`, `dequeue`, and `front`.

### Linked List Implementation
```javascript
class Node {
  constructor(element) {
    this.element = element;
    this.next = null;
  }
}

class LinkedList {
  constructor() {
    this.head = null;
    this.size = 0;
  }
  add(element) {
    let node = new Node(element);
    let current;

    if (this.head == null) this.head = node;
    else {
      current = this.head;
      while (current.next) {
        current = current.next;
      }
      current.next = node;
    }
    this.size++;
  }
}
```
- Shows a basic implementation of a linked list with a method for adding elements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
