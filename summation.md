# Summation Report

## Linked lists

  A linked list is a data structure where the objects are arranged in a linear order. Unlike an array, however, in which the linear order is determined by the array indices, the order in a linked list is determined by a pointer in each object.


## Problem:
To read the numbers from user untill **x** is not encountered and finally print the sum.

**Algorithm:**
<ol>
<li>Input numbers in character variable until "x" in encountered.</li>
<li>store the values entered by user in node of linked list after converting them into integer fron character data type.

**code**
```
cout << "Enter number to add and x to stop\n";
        cin >> ch;
    while (ch[0] != 'x' && ch[1] != '\0')
    {
        val = 0;
        len = strlen(ch) - 1;
        if (ch[0] == 'x' && ch[1] == '\0')
        {
            break;
        }
        for (int i = 0; i < strlen(ch); i++)
        {
            if (ch[i] >= '0' && ch[i] <= '9')
            {
                val = val + ((ch[i] - '0')) * pow(10, len);
                len--;
            }
        }
        push_back(val);
        cout << "Enter number to add and x to stop\n";
        cin >> ch;
    }

```
 </li>

<li>Lastly add all the values in linked list and display sum

**code**
```
p = head;
    while (p != NULL)
    {
        sum = sum + p->data;
        p = p->next;
    }
    cout << "sum=" << sum;
```
</li>