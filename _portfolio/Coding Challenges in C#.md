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
1. [Extract String within braces](#ExtractString)
1. [Find the missing integer in an array](#MissingInteger)
1. [Smallest lexicographical word](#LexicographicalWord)

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

    Example:

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

1. <a name="ExtractString"></a> Given an stream of characters consisting of letters and brackets, extract all sequence of letters enclosed by parentheses. The brackets in the stream are always in pairs and valid.

    Example: 
    ```bash
    # Input character stream :  (abc(d(e)f)) 
    # Expected output : 
    e
    def
    abcdef

    # Input character stream : abc(def(gh(i)j)kl)
    # Expected output :
    i
    ghij
    defghijkl

    # Input character stream: ((a)(b)cd(e)fg(h))ijk
    # Expected output :
    a
    b
    e
    h
    abcdefgh   
    ``` 
    Link to solution [code](https://github.com/Valliammai-Subramanian/coding-questions-in-csharp/tree/main/ExtractString).

1. <a name="MissingInteger"></a> Given an array A of N integers, return the smallest positive integer (greater than 0) that does not occur in A. N is an integer within the range [1..100,000]. Each element of array A is an integer within the range [−1,000,000..1,000,000].

    Example:
    ```bash
    # Input
    A = [1, 3, 6, 4, 1, 2]
    # Output
    5
    # Input
    A = [1, 2, 3]
    # Output
    4
    # Input
    A = [−1, −3]
    # Output
    1
    ``` 

    Link to solution [code](https://github.com/Valliammai-Subramanian/coding-questions-in-csharp/tree/main/MissingInteger).

1. <a name="LexicographicalWord"></a> Given a string S consisting of N characters, return the alphabetically smallest string that can be obtained by removing exactly one letter from S. Given S= "azb", by removing one letter, we can get "az","ab" or "zb". We should return "ab" (after removing 'z') since it is alphabetically smaller than "az" and "bz". N is an integer within the range [2..100,000]. String S consists only of lowercase letters (a-z).

    Example: 
    ```bash
    # Input string : bus 
    # Expected output : 
    bs
    
    # Input string : possibility
    # Expected output :
    ossibility

    # Input string: bbbbb
    # Expected output :
    bbbb   
    ``` 
    Link to solution [code](https://github.com/Valliammai-Subramanian/coding-questions-in-csharp/tree/main/LexicographicalWord).