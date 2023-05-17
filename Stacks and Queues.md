# Stacks and Queues
## Stack
### What is a 
A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.
First In Last Out (FILO)
Or
Last In First Out (LIFO)
* Push - Nodes or items that are put into the stack are pushed
* Pop - Nodes or items that are removed from the stack are popped. 
* Top - This is the top of the stack.
* Peek - When you peek you will view the value of the top Node in the stack. 

### Big (O) notation 
* Push O(1)
Pushing a Node onto a stack will always be an O(1) operation. This is because it takes the same amount of time no matter how many Nodes (n) you have in the stack.
* Pop O(1)
Popping a Node off a stack is the action of removing a Node from the top. 
* Peek O(1)
When conducting a peek, you will only be inspecting the top Node of the stack.

## Queue
### What is a 
First In First Out (FIFO)
Or
Last In Last Out (LILO)
Enqueue - Nodes or items that are added to the queue.
Dequeue - Nodes or items that are removed from the queue.
* Front - This is the front/first Node of the queue.
* Rear - This is the rear/last Node of the queue.
* Peek - When you peek you will view the value of the front Node in the queue. 

### Big (O) notation 
* Enqueue O(1)
* Dequeue O(1)
* Peek O(1)
