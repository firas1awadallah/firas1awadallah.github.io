# Linked Lists 
## what is Big O
Big O’s role in algorithm efficiency is to describe the Worst Case of efficiency an algorithm can have in performing it’s job. It specifically looks at the Running Time and Memory Space , which we often refer to as Space and Time. In order to analyze these limiting factors, we should consider 4 Key Areas for analysis:Input Size,Units of Measurement,Orders of Growth and Best Case, Worst Case, and Average Case.

## ## what is Linked Lists
A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.

* Head is always the first node in a Linked List
* Next contains the reference to the next node.
* One characteristic of linked lists is that they are linear data structures, which means that there is a sequence and an order to how they are constructed and traversed.


## Linked Lists types
1. Singly linked lists are the simplest type of linked list

2.  doubly linked list, because there are two references contained within each node: a reference to the next node, as well as the previous node.

3. circular linked list  , it has a node that acts as the tail of the list , and the node after the tail node is the beginning of the list.

## Linked Lists and Big O
 O(1) function takes constant time, which is to say that it doesn’t matter how many elements we have, or how huge our input is: it’ll always take the same amount of time and memory to run our algorithm.
O(n) function is linear, which means that as our input grows (from ten numbers, to ten thousand, to ten million), the space and time that we need to run that algorithm grows linearly.
O(n²) function, which clearly takes exponentially more time and memory the more elements that you have. 
