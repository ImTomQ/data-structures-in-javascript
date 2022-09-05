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

### [Types of Linked Lists](https://github.com/ImTomQ/data-structures-in-javascript#types-of-linked-lists)

There are two kinds of linked lists, **singly linked lists** and **doubly linked lists**. Both work very similarly, but the difference is in singly linked lists each node has a **single pointer** that indicates the **next node** on the list. While in doubly linked lists, each node has **two pointers**, one pointing to the **next node**, another pointing to the **previous node**.

![single linked list](/images/single-linked-list.png)

###### [In singly linked list each node has a single pointer](https://github.com/ImTomQ/data-structures-in-javascript#in-singly-linked-list-each-node-has-a-single-pointer)

Reference:
https://www.freecodecamp.org/news/implementing-a-linked-list-in-javascript/
https://www.freecodecamp.org/news/data-structures-in-javascript-with-examples/#linked-lists
https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#quoting-code
