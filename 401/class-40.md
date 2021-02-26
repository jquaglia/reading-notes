# Class 10

## Stacks and Queues

### What is a stack

A stack is a data structure that consists of `Nodes`. Each `Node` references the next Node in the stack, but does not reference its previous.

### Stack Terminology

1. Push - Nodes or items that are put into the stack are pushed

1. Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.

1. Top - This is the top of the stack.

1. Peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.

1. IsEmpty - returns true when stack is empty otherwise returns false.

### Stacks follow these concepts

- FILO - First In Last Out

- LIFO - Last In First Out

### Stack Visualization

![stack example](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG)

- Push O(1) - Pushing a Node onto a stack will always be an O(1) operation. This is because it takes the same amount of time no matter how many nodes you have in the stack.

- Pop O(1) - Popping a Node off a stack is the action of removing a node from the top. When conducting a pop, the top node will be re-assigned to the node that lives below and the top node is returned to the user.

- Peek O(1) - When conducting a peek, you will only be inspecting the top node of the stack.

- isEmpty O(1) - Returns a boolean value.

### What is a Queue

A queue is kind of like the opposite of a stack.

### Queue Terminology

1. Enqueue - Nodes or items that are added to the queue.

1. Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.

1. Front - This is the front/first Node of the queue.

1. Rear - This is the rear/last Node of the queue.

1. Peek - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.

1. IsEmpty - returns true when queue is empty otherwise returns false.

### Queue's follow these concepts

- FIFO - First In First Out

- LILO - Last In Last Out

### Queue visualization

![queue example](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Queue.PNG)

- Enqueue O(1) - When you add an item to a queue, you use the enqueue action. This is done with an O(1) operation in time because it does not matter how many other items live in the queue (n); it takes the same amount of time to perform the operation

- Dequeue O(1) - When you remove an item from a queue, you use the dequeue action. This is done with an O(1) operation in time because it doesn’t matter how many other items are in the queue, you are always just removing the front Node of the queue.

- Peek O(1) - When conducting a peek, you will only be inspecting the front Node of the queue.

- IsEmpty O(1) - Returns a boolean value.

[back to README](../README.md)
