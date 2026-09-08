

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:

```
EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST. Aim: To write a C program to display stack elements using linked list.

Algorithm:

Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
Declare a global variable head representing the starting node of the linked list.
Define a function display to print the elements of the linked list.
Declare a pointer p and initialize it with the head of the linked list.
Use a while loop to traverse the linked list:
Print the data of the current node.
Move to the next node using the next pointer.
Program:

//type your code here

Output:

//paste your output here

Result: Thus, the program to display stack elements using linked list is verified successfully.

EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST. Aim: To write a C program to pop an element from the given stack using liked list.

Algorithm:

Check for Empty Stack
If head is equal to NULL, Print "Stack is empty."
Else Proceed to the next step.
Set head to point to the next node in the stack.
Program:

//type your code here

Output:

//paste your output here

Result: Thus, the program to pop an element from the given stack using liked list is verified successfully.

EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST. Aim: To write a C program to display queue elements using linked list. Algorithm:

Check if Queue is Empty
Display Queue Elements
Print the data of the current node pointed to by front
Update front to point to the next node.
End the display function.
Program:

//type your code here

Output:

//paste your output here

Result: Thus, the program to display queue elements using linked list is verified successfully.

EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim: To write a C program to insert elements in queue using linked list

Algorithm:

Allocate Memory for New Node
Set Data and Next Pointer
Check if Queue is Empty
Set both front and rear to point to the new node p.
Set the next pointer of the current rear to point to the new node p.
End of Enqueue Operation
Program:

//type your code here

Output:

//paste your output here

Result: Thus, the program to insert elements in queue using linked list is verified successfully.

EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.

Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

Check if the queue is empty: o If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
Access the front element: o If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).
Program:

//type your code here

Output:

//paste your output here

Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.
```

Output:

```
Stack elements are:
30
20
10
```


Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *head = NULL;

void pop()
{
    struct Node *temp;

    if (head == NULL)
    {
        printf("Stack is empty.\n");
    }
    else
    {
        temp = head;
        printf("Popped element: %d\n", head->data);
        head = head->next;
        free(temp);
    }
}

void display()
{
    struct Node *p = head;

    printf("Stack elements are:\n");

    while (p != NULL)
    {
        printf("%d\n", p->data);
        p = p->next;
    }
}

int main()
{
    struct Node *p1, *p2, *p3;

    p1 = (struct Node *)malloc(sizeof(struct Node));
    p2 = (struct Node *)malloc(sizeof(struct Node));
    p3 = (struct Node *)malloc(sizeof(struct Node));

    p1->data = 30;
    p1->next = p2;

    p2->data = 20;
    p2->next = p3;

    p3->data = 10;
    p3->next = NULL;

    head = p1;

    printf("Stack before POP:\n");
    display();

    pop();

    printf("Stack after POP:\n");
    display();

    return 0;
}
```

Output:

```
Stack before POP:
Stack elements are:
30
20
10

Popped element: 30

Stack after POP:
Stack elements are:
20
10
```



Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *front = NULL;

void display()
{
    struct Node *p = front;

    if (front == NULL)
    {
        printf("Queue is empty.\n");
        return;
    }

    printf("Queue elements are:\n");

    while (p != NULL)
    {
        printf("%d\n", p->data);
        p = p->next;
    }
}

int main()
{
    struct Node *p1, *p2, *p3;

    p1 = (struct Node *)malloc(sizeof(struct Node));
    p2 = (struct Node *)malloc(sizeof(struct Node));
    p3 = (struct Node *)malloc(sizeof(struct Node));

    p1->data = 10;
    p1->next = p2;

    p2->data = 20;
    p2->next = p3;

    p3->data = 30;
    p3->next = NULL;

    front = p1;

    display();

    free(p1);
    free(p2);
    free(p3);

    return 0;
}
```

Output:

```
Queue elements are:
10
20
30
```

Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *front = NULL;
struct Node *rear = NULL;

void enqueue(int value)
{
    struct Node *p;

    p = (struct Node *)malloc(sizeof(struct Node));

    p->data = value;
    p->next = NULL;

    if (front == NULL)
    {
        front = p;
        rear = p;
    }
    else
    {
        rear->next = p;
        rear = p;
    }
}

void display()
{
    struct Node *temp = front;

    printf("Queue elements are:\n");

    while (temp != NULL)
    {
        printf("%d\n", temp->data);
        temp = temp->next;
    }
}

int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    display();

    return 0;
}
```

Output:

```
Queue elements are:
10
20
30
```

Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *front = NULL;

int peek()
{
    if (front == NULL)
    {
        printf("Queue is empty.\n");
        return -1;
    }

    return front->data;
}

int main()
{
    struct Node *p1, *p2, *p3;
    int value;

    p1 = (struct Node *)malloc(sizeof(struct Node));
    p2 = (struct Node *)malloc(sizeof(struct Node));
    p3 = (struct Node *)malloc(sizeof(struct Node));

    p1->data = 10;
    p1->next = p2;

    p2->data = 20;
    p2->next = p3;

    p3->data = 30;
    p3->next = NULL;

    front = p1;

    value = peek();

    if (value != -1)
        printf("Peek element of the queue: %d\n", value);

    free(p1);
    free(p2);
    free(p3);

    return 0;
}
```

Output:

```
Peek element of the queue: 10
```



Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


