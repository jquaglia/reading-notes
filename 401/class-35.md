# Class 05

## Linked Lists

### Terminology

- _Linked List_ - A data structure that contains nodes that links/points to the next node in the list.

- _Singly_ - Singly refers to the number of references the node has. A `Singly` linked list means that there is only one reference, and the reference points to the `Next` node in a linked list.

- _Doubly_ - Doubly refers to there being two (double) references within the node. A `Doubly` linked list means that there is a reference to both the `Next` and `Previous` node.

- _Node_ - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.

- _Next_ - Each node contains a property called `Next`. This property contains the reference to the next node.

- _Head_ - The Head is a reference type of type `Node` to the first node in a linked list.

- _Current_ - The `Current` reference is a reference type of type `Node` that is currently being looked at. This node is traditionally used when traversing through a full linked list. When traversing, you typically reset the current to the head to guarantee you are starting from the beginning of the linked list.

### What does it look like

This is what a Singly Linked List looks like
![image of Linked List](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/LinkedList1.PNG)

### Linear data structures

- One characteristic of linked lists is that they are linear data structures, which means that there is a sequence and an order to how they are constructed and traversed.

### Memory management

- The biggest differentiator between arrays and linked lists is the way that they use memory in our machines.

- When an array is created, it needs a certain amount of memory.

- On the other hand, when a linked list is born, it doesn’t need 7 bytes of memory all in one place.

### Parts of a linked list

- A linked list is made up of a series of nodes, which are the elements of the list.

- The starting point of the list is a reference to the first node, which is referred to as the head.

- The end of the list isn’t a node, but rather a node that points to null, or an empty value.

- It has just two parts: data, or the information that the node contains, and a reference to the next node.

### What is Big O

- Big O is really all over and omnipresent within computer science.

- computer science is all about efficiency and tradeoffs.

- The same goes for Big O Notation, but on a much lower level.

- Big O Notation is a way of evaluating the performance of an algorithm.

- There are two major points to consider when thinking about how an algorithm performs: how much time it requires at runtime given how much time and memory it needs.

## Growing a linked list

- unlike arrays, we don’t need to allocate memory in advance or copy and re-create our linked list, since we won’t “run out of space” the way we might with a pre-allocated array.

- all we really need to do is rearrange our pointers.

- We’ll start with the simplest place we can insert an element into a linked list: at the very beginning. This is fairly easy to do, since we don’t need to go through our entire list; instead we just start at the beginning.

    1. First, we find the head node of the linked list.

    1. Next, we’ll make our new node, and set its pointer to the current first node of the list.

    1. Lastly, we rearrange our head node’s pointer to point at our new node.

- Inserting an element at the beginning of a linked list is particularly nice and efficient because it takes the same amount of time, no matter how long our list is, which is to say it has a space time complexity that is constant, or O(1).

- But inserting an element at the end of a linked list is a different story. The interesting thing here is that the steps you take to actually do the inserting are the exact same

- we will need to find the last node. Which means that we’ll need to traverse through the entire linked list to find it. a linear O(n)

[back to README](../README.md)
