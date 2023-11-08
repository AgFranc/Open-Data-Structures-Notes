# resumenes
# re

### LINKED LIST INTRO

A linked list is a fundamental data structure in computer science and programming. It is used to store and organize a collection of elements, often referred to as nodes, in a linear, non-contiguous manner. Unlike arrays, linked lists do not require contiguous memory allocation, which makes them dynamic in size and provides flexibility for inserting and deleting elements.

In a linked list, each node consists of two parts:

1. Data: This part holds the actual value or data you want to store in the list.
2. Pointer (or reference): This part contains a reference to the next node in the list. In a singly linked list, each node points to the next node in the list. In a doubly linked list, each node has two pointers, one pointing to the next node and another pointing to the previous node.

The first node in a linked list is typically called the "head," and it serves as the starting point for traversing the list. The last node often has a reference to null (or "None" in some programming languages) to indicate the end of the list.

Linked lists come in several variations, including:

1. Singly Linked List: In a singly linked list, each node points to the next node in the list, forming a unidirectional chain.
2. Doubly Linked List: In a doubly linked list, each node has two pointers, one pointing to the next node and another pointing to the previous node. This allows for bidirectional traversal of the list.
3. Circular Linked List: In a circular linked list, the last node points back to the first node, creating a closed loop.

Linked lists are commonly used for various purposes in computer programming, such as implementing data structures like `stacks`, `queues`, and `symbol tables`. They are also essential in **memory management** and dynamic data structures because they can efficiently allocate and deallocate memory.

When working with linked lists, you can perform operations like `insertion, deletion, searching, and traversal`. It's important to manage the pointers properly to maintain the integrity of the list and to avoid memory leaks or access violations.

Here's a simple example of a singly linked list in Python:

```python
#PYTHON
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def append(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
        else:
            current = self.head
            while current.next:
                current = current.next
            current.next = new_node

```

```jsx
// JAVASCRIPT
class Node {
  constructor(data) {
    this.data = data;
    this.next = null;
  }
}

class LinkedList {
  constructor() {
    this.head = null;
  }

  append(data) {
    const newNode = new Node(data);
    if (!this.head) {
      this.head = newNode;
    } else {
      let current = this.head;
      while (current.next) {
        current = current.next;
      }
      current.next = newNode;
    }
  }
}

// Create a new linked list and append some elements
const myList = new LinkedList();
myList.append(1);
myList.append(2);
myList.append(3);

// Print the linked list
function printLinkedList(linkedList) {
  let current = linkedList.head;
  while (current) {
    console.log(current.data);
    current = current.next;
  }
}

printLinkedList(myList);
```

```java
//JAVA
class Node {
    int data;
    Node next;

    public Node(int data) {
        this.data = data;
        this.next = null;
    }
}

class LinkedList {
    Node head;

    public LinkedList() {
        this.head = null;
    }

    public void append(int data) {
        Node newNode = new Node(data);
        if (head == null) {
            head = newNode;
        } else {
            Node current = head;
            while (current.next != null) {
                current = current.next;
            }
            current.next = newNode;
        }
    }

    public void printList() {
        Node current = head;
        while (current != null) {
            System.out.print(current.data + " -> ");
            current = current.next;
        }
        System.out.println("null");
    }
}

public class Main {
    public static void main(String[] args) {
        LinkedList myList = new LinkedList();
        myList.append(1);
        myList.append(2);
        myList.append(3);

        System.out.println("Linked List:");
        myList.printList();
    }
}
```

This example demonstrates the basic structure of a singly linked list and how to append elements to it. You can extend it with other operations like inserting, deleting, or searching for nodes as needed.
