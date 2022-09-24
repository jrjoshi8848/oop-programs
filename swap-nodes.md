# Swap_nodes Reoprt

## Linked lists

 A linked list is a data structure where the objects are arranged in a linear order. Unlike an array, however, in which the linear order is determined by the array indices, the order in a linked list is determined by a pointer in each object.
  ### Node 
    Node is an object which contains the data for that node and location to the next node.
  ### NEXT   
   It is pointer in the node pointing to address of next node.
  #### Previous
   It is pointer int the node pointing to the address of previous node.
  ### Head
  It is pointer pointing to first node in linked list.

## Swapping Nodes
Swapping is the process of changing the position of two nodes with each others position.For this we have two ways ,
<ul>
   <li>Interchaging values contained in nodes without changing position of nodes.</li>
   <li>Interchanging position of nodes.</li>
  </ul>

## Swaping by Interchanging position of nodes.

**Algorithm:**
<ol>
<li>Serch node to be interchanged.</li>
<li>Locate the previous nodes of the nodes to be swapped .

**Code:**
```
while (node1->value != val1)
    {
        pre1 = node1;
        node1 = node1->next;
    }
    while (node2->value != val2)
    {
        pre2 = node2;
        node2 = node2->next;
    }
```

</li>
<li>Replacing next of previous node of each other. </li>
<li>Replacing next of each other.</li>
<li>In case of doubly linked list, we also replace the previous of the nodes to be swpped.

#### For single linked list

**code**
```
        pre1->next = node2;
        pre2->next = node1;
        ptr = node1->next;
        node1->next = node2->next;
        node2->next = ptr;
```

#### For dubly linked list

**code**
```
 node1->previous->next = node2;
            node2->previous->next = node1;
            node1->next->previous = node2;
            node2->next->previous = node1;
            ptr = node1->previous;
            node1->previous = node2->previous;
            node2->previous = ptr;
            ptr = node1->next;
            node1->next = node2->next;
            node2->next = ptr;
```
 </li>
</ol>

In this way the nodes will be swapped by interchanging their position.