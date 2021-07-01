
# Week 1 Linked list
### 1. Singly-Linked List

    head -> |-| -> |-| -> |-| -> |-| 
             7  -> 10  ->  4  ->  13

    ##### Node Contains  
    ##### k : Key value 
    ##### Next Pointer  
~~~C++
Template <typename T>
struct Node{
    T Key;
    struct Node* next_pointer;
};
~~~
### List API  
    PushFront(key)       : add to PushFront  
    T Topfront()         : return front item  
    PopFront()           : remove front item  
    PushBack(key)        : add to back also known as append  
    T TopBack()          : Return back item  
    PopBack()            : Remove back item  
    Boolean Find(key)    : is key in list ?  
    Erase(key)           : Remove key from list  
    Boolean Empty()      : empty list ?  
    AddBefore(Node, key) : adds key before Node  
    AddAfter(Node, key)  : adds key after Node  

### Times for Some operation
    PushFront           : O(1)  
    PopFront            : O(1)  
  
    PushBack (No tail)  : O(n) -> traversal  
    PopBack  (No tail)  : O(n) -> traversal  
    TopBack  (No tail)  : O(n) -> traversal  
  
    PushBack (with tail): O(1) -> no traversal with tail  
    PopBack  (with tail): O(n) -> traversal for previous Node of tail  
    TopBack  (with tail): O(1) -> no travsersal
  
    Find(Key)           : O(n) -> traversal  
    Erase(key)          : O(n) -> traversal  
    Empty()             : O(1) -> head != NULL or size element
    AddBefore           : O(n) -> traversal cauz previous Node  
    AddAfter            : O(1) -> no need traversal

### 2. Doubly Linked list


    head -> |-| <-> |-| <-> |-| <-> |-| <- tail
             7       10      4      13
        

    ##### Node Contains  
    ##### k : Key value 
    ##### Next Pointer  
    ##### prev Pointer
    ~~~C++
    Template <typename T>  
    struct Node{  
        T Key;  
        struct Node<T>* next_pointer;  
        struct Node<T>* prev_pointer;  
    };  
    ~~~
### Times for Some operation
    PushFront           : O(1)  
    PopFront            : O(1)  

    PushBack (No tail)  : O(n) -> traversal  
    PopBack  (No tail)  : O(n) -> traversal  
    TopBack  (No tail)  : O(n) -> traversal  

    PushBack (with tail): O(1) -> no traversal with tail  
    **PopBack  (with tail): O(1) -> no need traversal with prev pointer**  
    TopBack  (with tail): O(1) -> no travsersal

    Find(Key)           : O(n) -> traversal  
    Erase(key)          : O(n) -> traversal  
    Empty()             : O(1) -> head != NULL or size element
    **AddBefore         : O(1) -> no need traversal with prev pointer**   
    AddAfter            : O(1) -> no need travsersal 

### Summary
##### Constant time to insert at or remove from the pointer
##### With tail and doubly-linked, constant time to insert at or remove from the back
##### O(n) time to find elements
##### List elements need not be contiguous <-> array
##### with doubly-linked list(prev_pointer) -> constant time to insert between nodes or remove nodes
