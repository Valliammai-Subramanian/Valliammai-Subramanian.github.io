---
title: "Coding Challenges in C#"
excerpt: "Programming Trivia with Answers"
header:
  teaser: /assets/images/coding_questions_in_csharp_01.jpg
mathjax: true
feature_row:
  - image_path: /assets/images/coding_questions_in_csharp_02.jpg
  - image_path: /assets/images/coding_questions_in_csharp_03.jpg
  - image_path: /assets/images/coding_questions_in_csharp_04.jpg
gallery_04_01:
  - url: /assets/images/coding_questions_in_csharp_01.jpg.jpg
    image_path: /assets/images/coding_questions_in_csharp_01.jpg.jpg
  - url: /assets/images/coding_questions_in_csharp_02.jpg
    image_path: /assets/images/coding_questions_in_csharp_02.jpg
gallery_07_02:
  - url: /assets/images/coding_questions_in_csharp_03.jpg
    image_path: /assets/images/coding_questions_in_csharp_03.jpg
  - url: /assets/images/coding_questions_in_csharp_04.jpg
    image_path: /assets/images/coding_questions_in_csharp_04.jpg

date: "2020-10-19"
---

<!-- {% include feature_row %} -->

{% include toc %}

### Info
In this post, we will answer several programming challenge questions in C++. For easy testing of our single-file solutions, simply copy the entire source code and paste it into an online coding tool such as Coderpad at [https://coderpad.io/sandbox](https://coderpad.io/sandbox).

### Questions
{: .notice--success}
More programming challenge questions in C# will be added as time permits. Let me know if there is any particular problem you would like to have solved here.

1. [Array Sum](#ArraySum)
1. [Custom Stack](#CustomStack)

<!-- 1. [Match brackets in a string](#balancedBrackets)
1. [Sum of bits in 32-bit binary representation](#sumOfBits)
1. [Linked list - insert, delete, reverse](#linkedList)
1. [Longest continuous sequence](#longestContinuousSequence)
1. [Longest sequence](#longestSequence)
1. [Longest valid parentheses](#longestValidBrackets)
1. [Kth largest](#kthLargest)
1. [Mutatable priority queue](#mutatablePriorityQueue) -->

### Code
The [repository](https://github.com/Valliammai-Subramanian/coding-questions-in-csharp) contains the C# solution codes. To run each code type `dotnet run` in the command terminal.

### Solutions
1. <a name="ArraySum"></a> Given an array of integers, find its sum. The code should be time efficient to handle arrays of size upto 10^12. To solve this, the array is recursively divided into two halves and added in separate threads.

    Link to solution [code](https://github.com/Valliammai-Subramanian/coding-questions-in-csharp/tree/main/ArraySum).

1. <a name="CustomStack"></a> Implement the custom stack with the following features. The stack should have the extra feature to increament the elements from the bottom of the stack. All the elements in the stack will be integers.

    + push i: push integer i to the top of the stack
    + pop: pop out the top element of the stack
    + inc n x: increment n elements of the stack from the bottom by x

    After each operation, print the top of the stack. If the stack is empty, print "EMPTY"

    For Example:

      |Operations | Stack* | Output | 
      |-----------|--------|--------|
      |push 3     | [3]    |       3|
      |push 4     | [3,4]  |       4|
      |inc 2 1    | [4,5]  |       5|
      |pop        | [4]    |       4|
      |push 5     | [4,5]  |       5|
      |pop        | [4]    |       4|
      |pop        | []     |   EMPTY|
      
    *Note: Right most of the list is top of the stack

    Link to solution [code](https://github.com/Valliammai-Subramanian/coding-questions-in-csharp/tree/main/CustomStack).

<!-- 1. <a name="balancedBrackets"></a> Given a string containing just the characters '(', ')', '[', ']', '{', '}', determine if the input string is valid. An input string is valid if :
    + Open brackets must be closed by the same type of brackets.
    + Open brackets must be closed in the correct order.
  
    Note that an empty string is also considered valid. String below are considered valid strings.
    ```text
    ""
    "()"
    "()[]{}"
    "{[]}"
    ```
    Strings below are considered as invalid strings.
    ```text
    "["
    "}{"
    "{()"
    "(]"
    "([)]"
    ```

    Link to solution [code](https://github.com/Adaickalavan/coding-questions-in-cpp/blob/master/app/balancedBrackets.cpp).

1. <a name="sumOfBits"></a> Count the number of 1's in a binary representation of a 32bit integer. A look-up table or hash map which stores integers and their corresponding bit count is used to solve this problem. Several test cases are shown below.
    ```text
    Input: 1 // binary = 0000 0001
    Input: 5 // binary = 0000 0101
    Input: 15 // binary = 0000 1111
    Input: 19 // binary = 0001 0011
    Input: 22 // binary = 0001 0110
    ```
    Expected output:
    ```text
    Output: 1
    Output: 2
    Output: 4
    Output: 3
    Output: 3
    ```

    Link to solution [code](https://github.com/Adaickalavan/coding-questions-in-cpp/blob/master/app/sumOfBits.cpp).

1. <a name="linkedList"></a> Create a singly linked list with the following operations: insert at the tail, given a pointer delete the node (except the last node), and reverse.

    Link to solution [code](https://github.com/Adaickalavan/coding-questions-in-cpp/blob/master/app/linkedList.cpp).

1. <a name="longestContinuousSequence"></a> Given two strings, find the longest continuous sequence of characters common to the two strings. The problem is solved using dynamic programming pradigm. A testcase is as follows.
    ```cpp
    string str1 = "abcdefghijklmnopqrst";
    string str2 = "abcd3ekl3abfgs";
    ```
    Expected output:
    ```text
    Max elements: 4
    Max sequence: abcd
    ``` 
    
    Link to solution [code](https://github.com/Adaickalavan/coding-questions-in-cpp/blob/master/app/longestContinuousSequence.cpp). 

1. <a name="longestSequence"></a> Given two strings, find the longest continuous or non-continous sequence with same ordering of characters common to the two strings. The problem is solved using dynamic programming pradigm. A testcase is as follows.
    ```cpp
    string str1 = "abcdefghijklmnopqrst";
    string str2 = "abcd3ekl3abfgs";
    ```
    Expected output:
    ```text
    Max elements: 8
    ``` 
    
    Link to solution [code](https://github.com/Adaickalavan/coding-questions-in-cpp/blob/master/app/longestSequence.cpp). 

1. <a name="longestValidBrackets"></a> Given a string containing just characters '(' and ')', return the start and end indexes of the longest valid parentheses substring. Several test cases are shown below.
    ```text
    Input: "" // answer: startIndex = 0, endIndex = 0
    Input: "(()" // answer: startIndex = 1, endIndex = 2
    Input: ")()())" // answer: startIndex = 1, endIndex = 4
    Input: "())((())" // answer: startIndex = 4, endIndex = 7
    Input: "())(()" // answer: startIndex = 0, endIndex = 1
    ```
    Expected output:
    ```text
    Longest valid parentheses of  is   , from  0 to  0
    Longest valid parentheses of (() is () , from  1 to  2
    Longest valid parentheses of )()()) is ()() , from  1 to  4
    Longest valid parentheses of ())((()) is (()) , from  4 to  7
    Longest valid parentheses of ())(() is () , from  0 to  1
    ```
    Link to solution [code](https://github.com/Adaickalavan/coding-questions-in-cpp/blob/master/app/longestValidBrackets.cpp).

1. <a name="kthLargest"></a> Return the kth largest element, from an infinite stream of integers, at any point in time. The problem is solved using a priority queue. The priority queue is implemented by a minimum heap of size k. Read the top value of the heap to get the kth largest value at any point in time. Example input:
    ```cpp
    vector<int> stream = {10, 20, 11, 70, 50, 40, 100, 5, ...};
    int k = 3;
    ```
    Expected STDOUT output:
    ```bash
    $ -, -, 10, 11, 20, 40, 50, 50, ...
    ```
    Link to solution [code](https://github.com/Adaickalavan/coding-questions-in-cpp/blob/master/app/kthLargest.cpp).

1. <a name="mutatablePriorityQueue"></a> Build a priority queue whose elements' priority can be updated dynamically. This problem is solved using the following two data structures:
    + `unordered_map<>` functions as a `set` to hold all unique elements in the queue
    + `multimap<>` functions to hold all inserted elements sorted by priority

    Operation of the data structres is as follows:
    + New element, which is not present in `unordered_map<>`, is pushed into the `multimap<>` and `unordered_map<>`.
    + New element, which is present in `unordered_map<>`, is pushed into the `multimap<>` if it has a higher priority. Priority of the element in `unordered_map<>` is incremented to the higher value.
    + To `pop()` the highest priority element from the queue: Firstly, elements are sequentially removed from the top of the `multimap<>` until an element which is also present in `unordered_map<>` is reached. This helps remove duplicate entries present in `multimap<>`. Once reached, remove the element from both `multimap<>` and `unordered_map<>`. 

    Example testcase:
    ```cpp
    MutatablePriorityQueue mpq;
    mpq.push('a',3); // value: 'a', priority: 3
    cout << mpq.top() << "\n";
    mpq.push('b',4); // value: 'b', priority: 4
    mpq.push('c',3); // value: 'c', priority: 3
    cout << mpq.top() << "\n";
    mpq.push('a',5); // value: 'a', priority: 5
    cout << mpq.top() << "\n";
    mpq.pop();
    cout << mpq.top() << "\n";
    mpq.pop();
    cout << mpq.top() << "\n";
    ```
    Expected STDOUT output:
    ```bash
    a
    b
    a
    b
    c
    ```
    Link to solution [code](https://github.com/Adaickalavan/coding-questions-in-cpp/blob/master/app/mutatablePriorityQueue.cpp). -->