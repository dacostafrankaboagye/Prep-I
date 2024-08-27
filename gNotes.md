# Introduction

At the backbone of every program or piece of software are two entities

- data
- Algorithms

you can't ignore algorithms if you're hoping to write an innovative and efficient program

### How are data structures used?

Data structures handle four main functions for us:

- Inputting information

  - concerned with how the data is received.
  - What kind of information can be included?
  - Will the new data be added to the beginning, end, or somewhere in the middle of the existing data?
  - Does an existing point of data need to be updated or destroyed?

- Processing information

  - the way that data is manipulated in the data structure.
  - This can occur concurrently or as a result of other processes that data structures handle.
  - How does existing data that has been stored need to change to accommodate new, updated, or removed data?

- Maintaining information

  - focused on how the data is organized within the structure.
  - Which relationships need to be maintained between pieces of data?
  - How much memory must the system reserve (_allocate_) to accommodate the data?

- Retrieving information
  - devoted to finding and returning the data that is stored in the structure.
  - How can we access that information again?
  - What steps does the data structure need to take to get the information back to us?

### Note

- Different types and use cases for data will be better suited to different manners of the 4 functions
- This is why we have several data structures to choose from… and the ability to create our own!

**Choosing the best data structure**

- Choosing the wrong data structure can result in
  - slow or
  - unresponsive code (and mess up your program!)

1. What is the intended purpose for the data?

   - Do any data structures have built-in functionality that is ideally suited for this purpose?
   - Do you want to search, sort, or iterate data in a way in which certain data structures would be better suited than others?

2. Do you want or need control over how memory is set aside to store your data?

   - Data structures that use
     - *static memory allocation* (e.g., stacks or arrays) will manage memory for you and assume a fixed amount of memory upon instantiation with a cap on how much data may be added.
     - *dynamic memory allocation* (e.g., heaps or linked lists) allow you to allocate and reallocate memory within the life of the program.

   While memory allocation is not something that you’ll need to consider in languages like

   - Python or
   - Javascript

   (these languages will manage memory for you, regardless of which data structure you use),
   it is something to bear in mind when working in other languages like C.

3. How long will it take different data structures to accomplish various tasks relative to other data structures?
   - Technically, two data structures may both be able to accomplish the same task for you,
   - but one may be quite a bit faster.
   - This consideration, known as
     - *runtime* will be covered further in depth when you explore all the nifty tricks of asymptotic notation.

## Algorithm

- an algorithm is a step-by-step sequence of actions you need to perform to achieve the desired result.
- It is a set of instructions that can be expressed in various forms, such as natural language,
- flowcharts, pseudocode, or programming languages.

- Examples

  - It can be an algorithm for cooking a sandwich described by a recipe

  - Man is thinking of a sandwich.
  - Goes to the refrigerator, Open Refrigerator
  - Check if the refrigerator has ingredients.
  - Decision: Can a sandwich be made with available ingredients?
    - If Yes:
      - Take bread, fillings, and condiments
      - Arrange ingredients between slices of bread
      - That is your sanwich
    - If No:
      - Go to Grocery Store
      - Buy missing ingredients.
      - Make Sandwich.

- Computer Algorithms

  - Computer algorithms are everywhere around us.

    - smartphone is able to guide you through a city from one point to another using a certain algorithm

  - Algorithms are used to solve problems, make decisions, and perform tasks efficiently.

  - PathFinding

    - find the optimal path from a start point to a destination

      - navigation systems
      - Robotics
      - games

    - Birectional Search

      - for large maps
      - simultaneously searches from both the start and the goal, meeting in the middle

    - Dijkstra

      - network routing (Networks and Data Communication)
      - shortest path from a starting node to all other nodes

    - A\*
      - Dijkstra’s algorithm + heuristic to prioritize
      - Google Maps - I think

  - Video & photo processing

    - HEVC

      - High-Efficiency Video Coding
        - video - frame - blocks - compresses each block
        - we want video quality
      - Netflix, video conferencing

    - FFT (from engineering background)

      - In Engineering, what we want to do
      - Breaks down a signal into sine and cosine components at different frequencies
      - to process audio signals and image :: 4G, 5G

    - Voice Assistants (NLP):
      - Transformers
        - deep learning architecture that uses self-attention
      - BERT (Bidirectional Encoder Representations from Transformers)
      - GPT (Generative Pre-trained Transformer),

  Other Example

  - Autocorrect & Predictive Text:

## Algorithm

- To write any program with need an algorithm
- you need to choose one of several algorithms to solve a problem.

### Key Aspects / Characteristics

- Scalability
- The algorithm should maintain performance as input size grows.

- Correctness

  - The algorithm should provide the correct output for all valid inputs.

- Efficiency:
  - The algorithm should make optimal use of resources like time and memory.

## Notation

- it’s important to make smart programming choices so that code runs most efficiently.
- Computers seem to take no time evaluating programs,

  - but when scaling programs to deal with massive amounts of data, 
    - writing efficient code becomes the difference between success and failure.

- But We can’t just time the program

  - because different computers run at different speeds.

- Lets compare these two with:
    - differnt, processors, ram, 

look at left , right

  #### Different Processors (CPU)

  - clock speed, Cores and Threads

  ### Memory (RAM)

        - DDR4 - Double Data Rate 4 Synchronous Dynamic Random-Access Memory
        - DDR3 - Double Data Rate 3 Synchronous Dynamic Random-Access Memory

        Data Transfer rate, though all of them are Dynamic RAM
        - Non-Volatile Memory Express Solid State Drive.

  ### Graphics Card

       - RTX - Advance- AI... GTX - normal gaming

  - 1 trillion floating-point operations per second.

  - How do we measure efficiency?
    - Take note

- In computer science, we define how efficient a program is by its runtime.
- define runtime with asymptotic notatio → As it approaches infinity  

  ## Asymptotic Notation

  - With asymptotic notation,

    - we calculate a program’s runtime by looking at
    - how many instructions the computer has to perform

      - based on the size of the program’s input.

    - we can calculate a program’s runtime by looking at how
      - many instructions the computer has to perform
        - based on the size of the program’s input: N.


## Describing runtime

The first subtype of asymptotic notation

- Big Theta - is used when the runtime of an algorithm has only one case - that is - It describes the exact growth rate

            '''
            Function with input that is a list of size N:
               For each value in list:
                    Print the value

            '''


### Space

- Asymptotic notation

  - is often used to describe the runtime of a program or algorithm,

    - but it can also be used to describe the space, or memory, that a program or algorithm will need.

    """
    Like with time complexity, space complexity denotes space growth in relation to the input size.

💡 It’s also important to note that space complexity
usually refers to any additional space that will be needed,
and doesn’t count the space of the input.

            So a function could have 10 arrays passed into it,
            but if all it does inside is print **`"Hello World!"`**, then it still takes **`O(1)`** space
        """



## Array

- The array data structure is widely used in programming, Linear Data Structure
- The structure allows us to sequentially store a collection of elements of the same type and process them as a single unit.

- Operation

  - most frequently used method of array processing is accessing an element by its index.

- Fixed

  - the size of such an array is a constant:
    - once an array is created, you can't change its size.
    - computer then reserves necessary memory resources for the array.

- Dynamic

  - is able to grow and, in some implementations, shrink when its size changes

  - A dynamic array has two important properties:

    - size – the number of elements already stored in it;
    - capacity – a possible number of elements to
      - be stored that corresponds to the size of the internal regular array.

  - Scaling factor
    - If the number of elements exceeds the capacity,
      - all elements will be copied to a new internal array of a bigger size.



## Stack

- A DS that mimics a physical “stack” of objects.
- principle = elements are inserted and removed according to the last-in-first-out (LIFO)
- internal structure: linked list or a classic array

- A constraint that may be placed on a

  - stack is its size.

    - This is done to limit and quantify the

      - resources the data structure will take up when it is “full”.

      - Attempting to push data onto an already full stack will
        - result in a stack overflow.
      - Similarly, if you attempt to pop data from an empty stack,
        - it will result in a stack underflow.



## Queue
 - mimics a physical queue of objects like a line of people buying movie tickets

 - Enqueue
    - The operation when you insert anelement
        - the element is added by the REAR pointer. 
    
- Dequeue
    - If you remove an element, this operation is called dequeue, 
        - and the element that was pointed at by FRONT comes out of the queue. 
        
Note:
    - after any of these operations, the corresponding pointer moves.

## Linked list
-  represented as a sequence of connected nodes.
- the nodes are not required to be sequentially located in memory. 

 - The first node of a list is usually called the head.

  - Adding
    - at the top of the list
    - at the end of the list
    - at any other place specified by an index.

## Hash Map
 -  usefulness comes from specifying interrelationships within the data.
 - In order for a relationship to be a map, every key that is used can only be the key to a single value. 

 - In the case of a map between two things, we don’t really care about the exact sequence of the data.

  - If we turn it the other way: [the table] it would not be a MAP
  - We would still be able to describe that relationship with a table, but it wouldn’t be a map, and so we can’t save such a relationship using a hash map.


 Collision: [hash collison]
    - Remember hash functions are designed to compress data from a large number of possible keys to a much smaller range. Because of this compression, it’s likely that our hash function might produce the same hash for two different keys. This is known as a hash collision. There are several strategies for resolving hash collisions.

 - Hash collision strategy
     - Separate chanining
        -  Instead of an array of values that are mapped to by hashes, it could be an array of linked lists!
     - open addressing / linear probing:
        - we use array as the underline structurre: continuing to find new array indices in a fixed sequence until an empty index is found.

## Others
 - Trees
    - used to represent hierarchical relationships 
    - hierarchical structure with a root node and zero or more child nodes

- Tries (prefix tree)
    - specialized tree
        - ****Each node represents a character of a string, and paths from the root to leaves represent complete strings.


- Deque
    -  insertion and deletion of elements from both the front and back ends

    
- Treaps: A randomized binary search tree where nodes have priorities and maintain a balance between binary search tree properties and heap properties.

- Graph
    - nodes (vertices) connected by edges



- balanced binary search tre



Adjacency Matrix: A 2D array used to represent a graph where matrix entries indicate the presence or weight of edges between vertices.
