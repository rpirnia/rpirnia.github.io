---
layout: project
type: project
image: img/database.png
title: "Bank Database Application"
date: 2024
published: true
labels:
  - C
  - Vim
summary: "I created a bank database application entirely in C for ICS 212: Program Structures."
---

```cpp
*******************************
   Bank database application
*******************************

Menu options:
add      : Add a new record in the database
printall : Print all records in the database
find     : Find record(s) with a specified account number
delete   : Delete existing record(s) from the database using the account number as a key
quit     : Quit the program

Enter a command:

```
*Above are the commands the program offers*

This application uses a linked list to sort bank records. When you create a record, the program prompts you to enter an account number, name, and street address. The account number is used to sort the records in ascending order. No matter the organization of the list (whether inserting into an empty list, a list with one element, inserting between elements, etc.), the code performs properly. 

### Cleanup function
When the user chooses to quit the program, the cleanup function is called. cleanup() frees heap memory that was dynamically allocated while the program ran. This is essential, as it prevents memory leaks and dangling pointers. 

Let's say you added two records and then quit the program. Even though you exit the program, the records will remain sorted and accessible when you run the program again. cleanup() ensures proper memory management each time the user runs the program. 

**How does cleanup() work?** cleanup() takes the pointer to the head of the linked list, also known as the first element in the list, and traverses through the list freeing memory until it reaches the end of the list. 

```cpp
/****************************************************************
//
//  Function name: cleanup
//
//  DESCRIPTION:   Cleans heap memory
// 
//  Parameters:    start (struct record**) : pointer to a pointer
//                                           to the head of the 
//                                           linked list
//
//  Return values:  none
//
****************************************************************/

void cleanup(struct record ** start)
{
    struct record * temp = *start;
    struct record * temp2 = NULL;

   while (temp != NULL)
   {
       temp2 = temp->next;
       free(temp);
       temp = temp2;
   }

   *start = NULL;
}
```

### Future?
This was my first major project in C. I spent hours upon hours writing pseudocode, typing the code, and testing it. I am proud of what I learned about pointers, dynamic memory, and C in the process!

