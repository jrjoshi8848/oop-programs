#  Reversing Stack using recursion

##  Stack
A stack is a conceptual structure consisting of a set of homogeneous elements and is based on the principle of last in first out (LIFO). It is a commonly used abstract data type with two major operations, namely push and pop. Push and pop are carried out on the topmost element, which is the item most recently added to the stack. The push operation adds an element to the stack while the pop operation removes an element from the top position. The stack concept is used in programming and memory organization in computers.


**Algorithm:**
<ol>
<li>Create a recursive function to reverse the stack.</li>
<li>Pop the top element in each stack of recursion and hold the element in function call Stack until we reach the end of the stack. 

**code**
```
void reverse()
  {
    int t;
    t = pop();
    if (isEmpty())
    {
        push(t);
    }
    else
    {
        reverse();
        push_at_bottom(t);
    }
   }
```
</li>
<li>While moving back in the recursion tree, push the held element of each recursion call stack at the bottom of the stack.

**code**
```
void push_at_bottom(int t)
  {
    int t; 
    if (isEmpty())
    {
        push(t);
    }
    else
    {
        t = pop();
        push_at_bottom(t);
        push(t);
    }
   }
```


In this way our stack will be reversed.