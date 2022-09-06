# Data Structures in JavaScript With Examples

## [Linked List Data Structure](https://github.com/ImTomQ/data-structures-in-javascript#linked-list-data-structure)

> Linked lists are a type of data structure that store values in the form of a list.<br />

Unlike array, linked list elements are not stored at a contiguous location, the elements are linked using pointers.<br />
Within list, each value is considered a **node**, and each node is connected with the following value in the list (or null in case the element is the last in the list) through a **pointer**.<br />

The entry point to a linked list is called the **head**. The head is a reference to the first node in the linked list. The last node on the list points to null. If a list is empty, the head is null reference.

In Javascript, a linked list looks like this:

```
const list = {
    head: {
        value: 6
        next: {
            value: 10
            next: {
                value: 12
                next: {
                    value: 3
                    next: null
                    }
                }
            }
        }
    }
};
```

![linked list](/images/LLdrawio.png)

### [An advantage of Linked Lists](https://github.com/ImTomQ/data-structures-in-javascript#an-advantage-of-linked-lists)

Nodes can easily be removed or added from a linked list without reorganizing the entire data structure. **_This is advantage it has over arrays._**

### [Disadvantage of Linked lists](https://github.com/ImTomQ/data-structures-in-javascript#disadvantage-of-linked-lists)

- **_Search operations are slow in linked lists_**. Unlike arrays, random access of data elements is not allowed. Nodes are accessed sequentially starting from the first node.
- It uses more memory than arrays because of the storage of the pointers.

### [Types of Linked Lists](https://github.com/ImTomQ/data-structures-in-javascript#types-of-linked-lists)

There are two kinds of linked lists, **singly linked lists** and **doubly linked lists**. Both work very similarly, but the difference is in singly linked lists each node has a **single pointer** that indicates the **next node** on the list. While in doubly linked lists, each node has **two pointers**, one pointing to the **next node**, another pointing to the **previous node**.

![single linked list](/images/single-linked-list.png)

###### [In singly linked list each node has a single pointer](https://github.com/ImTomQ/data-structures-in-javascript#in-singly-linked-list-each-node-has-a-single-pointer)

### Implementing a List Node in JavaScript

As started earlier, a list node contains two items: the data and the pointer to the next node. We can implement a list node in JavaScript as follows:

```
class ListNode {
    constructor(data) {
        this.data = data
         this.next = null
    }
}
```

### Implementing a Linked List in JavaScript

The code below shows the implementation of a linked list class with a constructor.
Notice that if the head node is not passed, the head node is initialised to null.

```
class LinkedList {
    constructor(head = null) {
        this.head = head
    }
}
```

Let's create a linked list with the class we just created. First, we create two list nodes, node1, node2 and a pointer from node1 to node2.

```
let node1 = new ListNode('node1');
let node2 = new ListNode('node2');

node1.next = node2;
```

Next, we'll create a linked list with node1.

```
let list = new LinkedList(node1)

console.log(list) // return head: ListNode { data: 2, next: ListNode { data: 5, next: null } }

console.log(list.head.next.data) // return 'node2'
```

### Some LinkedList methods

Next up, we will implement four helper methods for linked list. They are:

- size()
- clear()
- getLast()
- getFirst()

#### 1. size()

This method returns number of nodes present in the linked list.

```
size() {
    let count = 0;
    let node = this.head;
    while (node) {
        count++;
        node = node.next
    }
    return count;
}
```

#### 2. clear()

This method empties out the list.

```
clear() {
    this.head = null;
}
```

#### 3. getLast()

This method returns the last node of the linked list.

```
getLast() {
    let lastNode = this.head;
    if (lastNode) {
        while (lastNode.next) {
            lastNode = lastNode.next
        }
    }
    return lastNode
}
```

#### 4. getFirst()

This method returns the first node of the linked list.

```
getFirst() {
    return this.head;
}
```

**_Reference:_**

- https://www.freecodecamp.org/news/implementing-a-linked-list-in-javascript/
- https://www.freecodecamp.org/news/data-structures-in-javascript-with-examples/#linked-lists
- https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#quoting-code
