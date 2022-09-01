# Data Structures in JavaScript With Examples

## Linked List Data Structure

> Linked lists are a type of data structure that store values in the form of a list.<br />

Unlike array, linked list elements are not stored at a contiguous location, the elements are linked using pointers.<br />
Within list, each value is considered a **node**, and each node is connected with the following value in the list (or null in case the element is the last in the list) through a **pointer**.<br />

![linked list](/images/LLdrawio.png)

### Types of Linked Lists

There are two kinds of linked lists, **singly linked lists** and **doubly linked lists**. Both work very similarly, but the difference is in singly linked lists each node has a **single pointer** that indicates the **next node** on the list. While in doubly linked lists, each node has **two pointers**, one pointing to the **next node**, another pointing to the **previous node**.

![single linked list](/images/single-linked-list.png)

###### In singly linked list each node has a single pointer
