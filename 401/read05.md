# [Linked List](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)





### Definitios : 

- Is a grou of nodes that are connected to each other , and each node have data and reference that refers to the next node .
- Two types of linked lists : singly , doubly .

## Add a node after a given value:

If you want to add a node after a given value, follow these steps:

1. Add a current node that points at the current node and assign it to the head.
2. Create a new node for the value
3. Then by using while loop and current.next loop through the linked list
4. Create a condition to check if the current node is equal to the value
5. First add a reference for the new node to the current node.next
6. Then change the reference for the current node to the new node



### Implementation :
- When traversing a linked list we cant use a for or for each loop .
- We use the next reference which will guid us where the next node occurs .
- A good traversing can be implemented using the while loop until the next reference is null .
- if we reached a node that is null A nullReferenceException will be thrown .
- The current will guide us where are we on the node list .


## What are Linked Lists :
### Linear data structures :
- Linear data structure is modeling the data sequentially so to reach the last one you have to traverse each element .
- Non - linear data structres are non-sequential data representation .

### When to use list and when not :

- Linked list is a good approach when adding or removing most elements .

- It's slow in searching and finding or modifying elements .

- Linked lists are faster to insert and delete elements .

- Slow to search in a linked list (an array is a better approach in this case ) .

- Have dynamic size to shrink or grow .

- Only allocates memory as required during the runtime .

- Finding an element requires traversal through the linked list .

### [Big O :](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html)

- Is the way to calculate how efficent an algorithm is .

- It's used to determine how effictive an algorithm is in the terms of time and space .

- Big O referes to an order and n refers to number of elements in the algorithm .
