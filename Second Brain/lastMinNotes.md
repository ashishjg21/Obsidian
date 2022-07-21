### 1. What are the different data types present in C++?

The 4 data types in C++ are given below:

-   Primitive Datatype(basic datatype). Example- char, short, int, float, long, double, bool, etc.
-   Derived datatype. Example- array, pointer, etc.
-   Enumeration. Example- enum
-   User-defined data types. Example- structure, class, etc.


C is a procedure-oriented programming language.
C++ is an object-oriented programming language.

**Operator Overloading** is a very essential element to perform the operations on user-defined data types. By operator overloading we can modify the default meaning to the operators like +, -, *, /, <=, etc.

A **friend class** can access private, protected, and public members of other classes in which it is declared as friends.

If a function is **inline** , the compiler places a copy of the code of that function at each point where the function is called at compile time. One of the important advantages of using an inline function is that it eliminates the function calling overhead of a traditional function.

A **reference** is like a pointer. It is another name of an already existing variable. Once a reference name is initialized with a variable, that variable can be accessed by the variable name or reference name both.

### What is an abstract class and when do you use it?
A class is called an abstract class whose objects can never be created. Such a class exists as a parent for the derived classes. We can make a class abstract by placing a pure virtual function in the class.

### What is this pointer in C++?
The member functions of every object have a pointer named this, which points to the object itself. The value of this is set to the address of the object for which it is called. It can be used to access the data in the object it points to.


# git
###  Uses of Git

-   Git is used to tracking changes in the source code.
-   Distributed version control tool used for source code management.
-   Allows multiple developers to work together.
-   Supports non-linear development because of its thousands of parallel branches.

-   Create a local branch and switch to that branch:

```plaintext
git checkout -b <branch_name>
```

-   Push in the local branch:

```plaintext
git push -u origin <branch_name>
```

To **delete remote branches**, use the following command:

```plaintext
git push origin --delete <branch_name>
```

# dsa
-   The difference is that storage structure has data stored in the memory of the computer system, whereas file structure has the data stored in the auxiliary memory.
#### What is a linked list?

A linked list is a data structure that has **sequence of nodes** where every node is connected to the next node by means of a reference pointer. The elements are **not stored in adjacent** memory locations. They are linked using pointers to form a chain. This forms a chain-like link for data storage
-   Each node element has two parts:
	-   a data field
	-   a reference (or pointer) to the next node.

#### Q: Are linked lists of linear or non-linear type?

Linked lists can be considered both linear and non-linear data structures. This depends upon the application that they are used for.

-   When linked list is used for access strategies, it is considered as a linear data-structure. When they are used for data storage, it can be considered as a non-linear data structure


#### Q: Explain the scenarios where you can use linked lists and arrays.

-   Following are the scenarios where we use linked list over array:
    -   When we do not know the exact number of elements beforehand.
    -   When we know that there would be large number of add or remove operations.
    -   Less number of random access operations.
    -   When we want to insert items anywhere in the middle of the list, such as when implementing a priority queue, linked list is more suitable.
-   Below are the cases where we use arrays over the linked list:
    -   When we need to index or randomly access elements more frequently.
    -   When we know the number of elements in the array beforehand in order to allocate the right amount of memory.
    -   When we need speed while iterating over the elements in the sequence.
    -   When memory is a concern:
        -   Due to the nature of arrays and linked list, it is safe to say that filled arrays use less memory than linked lists.
        -   Each element in the array indicates just the data whereas each linked list node represents the data as well as one or more pointers or references to the other elements in the linked list.
-   To summarise, requirements of space, time, and ease of implementation are considered while deciding which data structure has to be used over what.

#### doubly-linked list (DLL)
-   This is a complex type of a linked list wherein a node has two references:
    -   One that connects to the next node in the sequence
    -   Another that connects to the previous node.
-   This structure allows traversal of the data elements in both directions (left to right and vice versa).
-   Applications of DLL are:
    1.  A music playlist with next song and previous song navigation options.
    2.  The browser cache with BACK-FORWARD visited pages
    3.  The undo and redo functionality on platforms such as word, paint etc, where you can reverse the node to get to the previous page.#### doubly-linked list (DLL)#### doubly-linked list (DLL)

#### applications of a stack:

1.  Check for balanced parentheses in an expression
2.  Evaluation of a postfix expression
3.  Problem of Infix to postfix conversion
4.  Reverse a string

#### applications of queue are:

1.  CPU Task scheduling
2.  BFS algorithm to find shortest distance between two nodes in a graph.
3.  Website request processing
4.  Used as buffers in applications like MP3 media player, CD player, etc.
5.  Managing an Input stream

#### How to implement a queue using stack?

-   A queue can be implemented using **two stacks**. Let `q` be the queue and`stack1` and `stack2` be the 2 stacks for implementing `q`. We know that stack supports push, pop, peek operations and using these operations, we need to emulate the operations of queue - enqueue and dequeue. Hence, queue `q` can be implemented in two methods (Both the methods use auxillary space complexity of O(n)):
    1.  **By making enqueue operation costly:**
        -   Here, the oldest element is always at the top of `stack1` which ensures dequeue operation to occur in O(1) time complexity.
        -   To place element at top of stack1, stack2 is used.
        -   **Pseudocode:**
            
            -   Enqueue: Here time complexity will be O(n)
                
                enqueue(q, data):
                  While stack1 is not empty:
                      Push everything from stack1 to stack2.
                      Push data to stack1
                      Push everything back to stack1.
                
            -   Dequeue: Here time complexity will be O(1)
                
                deQueue(q):
                  If stack1 is empty then error
                  else
                      Pop an item from stack1 and return it
                
    2.  **By making dequeue operation costly:**
        -   Here, for enqueue operation, the new element is pushed at the top of `stack1`. Here, the enqueue operation time complexity is O(1).
        -   In dequeue, if `stack2` is empty, all elements from `stack1` are moved to `stack2` and top of `stack2` is the result. Basically, reversing the list by pushing to a stack and returning the first enqueued element. This operation of pushing all elements to new stack takes O(n) complexity.
        -   **Pseudocode:**
            -   Enqueue: Time complexity: O(1)
                
                enqueue(q, data):
                    Push data to stack1
                
            -   Dequeue: Time complexity: O(n)
                
                dequeue(q):
                    If both stacks are empty then raise error.
                    If stack2 is empty:
                         While stack1 is not empty:
                             push everything from stack1 to stack2.
                    Pop the element from stack2 and return it.

#### How do you implement stack using queues?
-   A stack can be implemented using two queues. We know that a queue supports enqueue and dequeue operations. Using these operations, we need to develop push, pop operations.
-   Let stack be ‘s’ and queues used to implement be ‘q1’ and ‘q2’. Then, stack ‘s’ can be implemented in two ways:
    1.  **By making push operation costly:**
        -   This method ensures that newly entered element is always at the front of ‘q1’, so that pop operation just dequeues from ‘q1’.
        -   ‘q2’ is used as auxillary queue to put every new element at front of ‘q1’ while ensuring pop happens in O(1) complexity.
        -   **Pseudocode:**
            -   Push element to stack s : Here push takes O(n) time complexity.
                
                push(s, data):
                    Enqueue data to q2
                    Dequeue elements one by one from q1 and enqueue to q2.
                    Swap the names of q1 and q2
                
            -   Pop element from stack s: Takes O(1) time complexity.
                
                pop(s):
                    dequeue from q1 and return it.
                
    2.  **By making pop operation costly:**
        -   In push operation, the element is enqueued to q1.
        -   In pop operation, all the elements from q1 except the last remaining element, are pushed to q2 if it is empty. That last element remaining of q1 is dequeued and returned.
        -   **Pseudocode:**
            -   Push element to stack s : Here push takes O(1) time complexity.
                
                push(s,data):
                    Enqueue data to q1
                
            -   Pop element from stack s: Takes O(n) time complexity.
                
                pop(s):
                    Step1: Dequeue every elements except the last element from q1 and enqueue to q2.
                    Step2: Dequeue the last item of q1, the dequeued item is stored in result variable.
                    Step3: Swap the names of q1 and q2 (for getting updated data after dequeue)
                    Step4: Return the result.

