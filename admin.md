To be able to sent command, we need to be able to track nodes. 
As node are free to send the package to whatever next node they want, it is impossible to keep an organized list of where each node has sent the package.

What could happen is that we could treat each node as part of a Linked List. In a Linked List Data structure, each node can keep track of what is the next node that they has
sent the package to. This is mean that a node only knows of its existence and the node it sent the package to. 

When we want to sent a command over a specific node, we first find the node we first pass the package to and give it a command, a counter number, and a desired number. 
We instruct the node to check if the counter it got matches the desired, if not increase the counter by one and passed the command, counter, and the desired to its next node. We will also pass the instruction for the next node to repeat as well.
However, if the counter and desired does match, then we instruct the node to excute the command. 

This works great for if there is only a single package to keep track of. However, since a node can recieve multiple package, then we should also instruct the node to keep 
track what package it recieved and which node it passed the package to. This will allow for the node to knows where the where it sent each package if it has recieved multiple packages.

A graphical representation of how this system could be:

![Example Node Tree](/InsertingMinHeap%20(2).PNG)
