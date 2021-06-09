
# Read 5

## Linked Lists

-A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.

-There are two types of Linked List - Singly and Doubly. We will be implementing a Singly Linked List in this implementation.

-Linked List - A data structure that contains nodes that links/points to the next node in the list.

-Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.

-Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

-Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.

-Next - Each node contains a property called Next. This property contains the reference to the next node.

-Head - The Head is a reference type of type Node to the first node in a linked list.

-Current - The Current reference is a reference type of type Node that is currently being looked at. This node is traditionally used when traversing through a full linked list. When traversing, you typically reset the current to the head to guarantee you are starting from the beginning of the linked list.

-When traversing a linked list, you are not able to use a foreach or for loop. We depend on the Next value in each node to guide us where the next reference is pointing. The Next property is exceptionally important because it will lead us where the next node is and allow us to extract the data appropriately.

-The best way to approach a traversal is through the use of a while() loop. This allows us to continually check that the Next node in the list is not null. If we accidentally end up trying to traverse on a node that is null, a NullReferenceException gets thrown and our program will crash/end.

-When traversing through a linked list, the Current node is the most helpful. The Current will tell us where exactly in the linked list we are and will allow us to move/traverse forward until we hit the end.

-The Big O of time for Includes would be O(n). This is because, at its worse case, the node we are looking for will be the very last node in the linked list. n represents the number of nodes in the linked list.

-The Big O of space for Includes would be O(1). This is because there is no additional space being used than what is already given to us with the linked list input.

-Order of operations is extremely important when it comes to working with a Linked List. What I mean by this is you must be careful that all references to each link/node is properly assigned.

-Regardless of the number of Nodes that this linked list has, it will always be a O(1) time and space because it takes the same amount of time to add a new node to the beginning of the list, and no additional resources are being used.

-Printing out all of the nodes in a Linked List is very similar to what we did in the Find() method. This is because we are leveraging our Current node and a while loop to traverse through the existing linked list.

-When making your Node class, consider requiring a value to be passed in to require that each node has a value.

-When making a Linked List, you may want to require that at least one node gets passed in upon instantiation. This first node is what your Head and Current will point too.
