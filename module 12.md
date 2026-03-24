

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
struct Node   
{  
    char data[100];  
    struct Node *next;  
}*head;  
void display()  
{
    struct Node *current=head;
    while(current!=NULL)
    {
        printf("%s\n",current->data);
        current=current->next;
    }
}
```


Output:

<img width="600" height="594" alt="image" src="https://github.com/user-attachments/assets/842adcec-e608-4639-a518-acfed55a92b7" />


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

struct Node   
{  
    float data;  
    struct Node *next;  
}*head;  
void pop()  
{  
    struct Node *ptr=head;  
    if(head==NULL)  
    {  
        printf("stack is empty");  
    }  
    else  
    {  
        head=head->next;
        free(ptr);
        ptr=NULL;
    }  
}
```

Output:

<img width="851" height="476" alt="image" src="https://github.com/user-attachments/assets/1f15d075-f767-4e6e-b240-1e03344174dc" />




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
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    struct Node *current=front;
    if(front==NULL)
    {
        printf("queue is empty");
        return;
    }
    else
    {
        printf("Queue elements:\n");  
        while(current!=NULL)
        {
            printf("%.3f\n",current->data);
            current=current->next;
        }
    }
}
```

Output:

<img width="731" height="663" alt="image" src="https://github.com/user-attachments/assets/a93ddd2c-be19-4af4-85bc-57a8ef93503c" />


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
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(int data)
{
    struct Node *current=malloc(sizeof(struct Node));
    current->data=data;
    current->next=NULL;
    if(front==NULL)
    {
        front=rear=current;
    }
    else
    {
        rear->next=current;
        rear=current;
    }
}
```

Output:
<img width="707" height="642" alt="image" src="https://github.com/user-attachments/assets/20b3d938-8b88-4f6e-880a-91aa233ad407" />


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
struct Node   
{  
    float data;  
    struct Node *next;  
}*head;
void peek()
{
    struct Node *current=head;
    printf("%.2f",current->data);
}
```

Output:


<img width="590" height="487" alt="image" src="https://github.com/user-attachments/assets/13b1ca9f-304e-423b-8286-8f38acf83a75" />



Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


