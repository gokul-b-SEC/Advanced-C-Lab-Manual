EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

```
#include <stdio.h>

#define SIZE 5

int stack[SIZE];
int top = -1;

void display()
{
    int i;

    if (top == -1)
    {
        printf("Stack is empty.\n");
        return;
    }

    printf("Stack elements are:\n");

    for (i = top; i >= 0; i--)
    {
        printf("%d\n", stack[i]);
    }
}

int main()
{
    stack[0] = 10;
    stack[1] = 20;
    stack[2] = 30;
    stack[3] = 40;

    top = 3;

    display();

    return 0;
}
```

Output:

```
Stack elements are:
40
30
20
10
```



Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

```
#include <stdio.h>

#define SIZE 5

float stack[SIZE];
int top = -1;

void push(float value)
{
    if (top == SIZE - 1)
    {
        printf("Stack Overflow.\n");
    }
    else
    {
        top++;
        stack[top] = value;
        printf("%.2f pushed into the stack.\n", value);
    }
}

void display()
{
    int i;

    printf("Stack elements are:\n");

    for (i = top; i >= 0; i--)
    {
        printf("%.2f\n", stack[i]);
    }
}

int main()
{
    float value;

    printf("Enter the element to push: ");
    scanf("%f", &value);

    push(value);

    display();

    return 0;
}
```

Output:

```
Enter the element to push: 25.5
25.50 pushed into the stack.
Stack elements are:
25.50
```




Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

```
#include <stdio.h>

#define SIZE 5

int queue[SIZE];
int front = 0;
int rear = 3;

void display()
{
    int i;

    if (front > rear)
    {
        printf("Queue is empty.\n");
        return;
    }

    printf("Queue elements are:\n");

    for (i = front; i <= rear; i++)
    {
        printf("%d\n", queue[i]);
    }
}

int main()
{
    queue[0] = 10;
    queue[1] = 20;
    queue[2] = 30;
    queue[3] = 40;

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
40
```


Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```
#include <stdio.h>

#define SIZE 5

float queue[SIZE];
int front = 0;
int rear = -1;

void enqueue(float value)
{
    if (rear == SIZE - 1)
    {
        printf("Queue Overflow.\n");
    }
    else
    {
        rear++;
        queue[rear] = value;
        printf("%.2f inserted into the queue.\n", value);
    }
}

void display()
{
    int i;

    printf("Queue elements are:\n");

    for (i = front; i <= rear; i++)
    {
        printf("%.2f\n", queue[i]);
    }
}

int main()
{
    float value;

    printf("Enter the element to insert: ");
    scanf("%f", &value);

    enqueue(value);

    display();

    return 0;
}
```

Output:

```
Enter the element to insert: 35.5
35.50 inserted into the queue.
Queue elements are:
35.50
```

Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

```
#include <stdio.h>

#define SIZE 5

int queue[SIZE] = {10, 20, 30, 40};
int front = 0;
int rear = 3;

void deleteElement()
{
    if (front == -1)
    {
        printf("Queue is empty.\n");
    }
    else
    {
        printf("Deleted element: %d\n", queue[front]);

        front++;

        if (front > rear)
        {
            front = -1;
            rear = -1;
        }
    }
}

void display()
{
    int i;

    if (front == -1)
    {
        printf("Queue is empty.\n");
        return;
    }

    printf("Queue elements are:\n");

    for (i = front; i <= rear; i++)
    {
        printf("%d\n", queue[i]);
    }
}

int main()
{
    printf("Queue before deletion:\n");
    display();

    deleteElement();

    printf("Queue after deletion:\n");
    display();

    return 0;
}
```

Output:

```
Queue before deletion:
Queue elements are:
10
20
30
40

Deleted element: 10

Queue after deletion:
Queue elements are:
20
30
40
```


Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
