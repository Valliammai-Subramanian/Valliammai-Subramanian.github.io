---
title: "Coding Challenges in Golang"
excerpt: "Programming Trivia with Answers"
header:
  teaser: /assets/images/coding_questions_in_golang_01.jpg
mathjax: true
feature_row:
  - image_path: /assets/images/coding_questions_in_golang_02.jpg
  - image_path: /assets/images/coding_questions_in_golang_03.jpg
  - image_path: /assets/images/coding_questions_in_golang_04.jpg
gallery_04_01:
  - url: /assets/images/coding_questions_in_golang_01.jpg
    image_path: /assets/images/coding_questions_in_golang_01.jpg
  - url: /assets/images/coding_questions_in_golang_02.jpg
    image_path: /assets/images/coding_questions_in_golang_02.jpg
gallery_07_02:
  - url: /assets/images/coding_questions_in_golang_03.jpg
    image_path: /assets/images/coding_questions_in_golang_03.jpg
  - url: /assets/images/coding_questions_in_golang_04.jpg
    image_path: /assets/images/coding_questions_in_golang_04.jpg

date: "2021-07-31"
---

<!-- {% include feature_row %} -->

{% include toc %}

### Info
In this post, we will answer several programming challenge questions in Golang. For easy testing of our single-file solutions, simply copy the entire source code and paste it into an online coding tool such as Coderpad at [https://coderpad.io/sandbox](https://coderpad.io/sandbox).

### Questions
{: .notice--success}
More programming challenge questions in Golang will be added as time permits. Let me know if there is any particular problem you would like to have solved here.

1. [Find Absolute difference in a square matrix](#absDiff)
1. [Breadth First Search & Depth First Search](#bfsDfs)
1. [Given two sorted lists, merge them into a single sorted list](#Concatenate)
1. [K-Means Clustering algorithm](#kMeans)
1. [Reformatting a string](#Reformat)
1. [Reverse a string](#stringReverse)
1. [Find the substring from a list of strings](#Substring)

### Code
The [repository](https://github.com/Valliammai-Subramanian/coding-questions-in-golang) contains the Golang solution codes. To run each code type `go run .` in the command terminal.

### Solutions
1. <a name="absDiff"></a> Given a square matrix of integers, find its absolute difference. The code should be time efficient to handle large matrices and matrices with negative elements.

    Link to solution [code](https://github.com/Valliammai-Subramanian/coding-questions-in-golang/tree/main/absDiff).

1. <a name="bfsDfs"></a>Traverse a tree, in a breadth first and depth first manner, from the starting node till the ending node. The first node, namely `node1`, is the starting node. The node with a field value `end:true` marks the ending node. Return true if an end node is reached, else return false. Remember to avoid possible cycles in the tree.

    Example input tree:
    ```text
    Tree structure
                    node1
                      |
            ---------------------
            |                   |
          node2               node 3
            |                   |
        -----------             |
        |         |             |
      node4     node5         node 6
                  |
             -----------
             |         |
           node7     node8
    ```
    Expected output:
    ```text
    Breath first search = 1 2 3 4 5 6 7 8 true
    Depth first search = 1 2 4 5 7 8 true
    ```

    Link to solution [code](https://github.com/Valliammai-Subramanian/coding-questions-in-golang/tree/main/bfsDfs).

1. <a name="Concatenate"></a> Given two sorted lists, merge them into a single sorted list.

    Link to solution [code](https://github.com/Valliammai-Subramanian/coding-questions-in-golang/tree/main/concatenate).

1. <a name="kMeans"></a>Given a list of data points and a list of centroids, perform K-Means clustering to return a new set of updated centroids. Goroutines are used to parallelize the code execution.

    Link to solution [code](https://github.com/Valliammai-Subramanian/coding-questions-in-golang/tree/main/kMeans).

1. <a name="Reformat"></a> Given a string S representing a number consisting of N characters: digits, spaces/dashes. It contains atleast two digits. Spaces and the dashes in the string can be ignored. The string should be reformatted in such a way that the digits are grouped in blocks of length three, seperated by single dashes. If necessary the final block or the last two blocks can be of length two.

    Example: 
    ```bash
    # Input string : 00-12  26 8888 5361 
    # Expected output : 
    001-226-888-853-61
    
    # Input string : 0 - 11 2987--324
    # Expected output :
    011-298-73-24

    # Input string: 666372354
    # Expected output :
    666-372-354   
    ``` 
    Link to solution [code](https://github.com/Valliammai-Subramanian/coding-questions-in-golang/tree/main/reformat).

1. <a name="stringReverse"></a> Reverse a given string. The string is reversed in parallel using goroutines and channels.

    Link to solution [code](https://github.com/Valliammai-Subramanian/coding-questions-in-golang/tree/main/stringReverse).

1. <a name="Substring"></a>Array A contains a sequence of names and array B contains numbers corresponding to the names in array A. Given a string S of length N representing a partial number, find the name whose number contains S as a contiguous substring. For example, "5900" is a contiguous substring of "43590012", whereas "3514" is not a contiguous substring.

    If there is more than one name matching the search criteria, return the alphabetically smallest name.

    If no match is found, return "NO MATCH".

    Example:

    ```bash
    # Input arrays : A=["sam","sha"], B=["888888888","555777888"] and P="77888"
    # Expected output : 
    sha
    
    # Input arrays : A=["shan","aemy","anna","mike"], B=["123456789","234567890","789123456","431431431"] and P="1"
    # Expected output :
    anna

    # Input arrays: A=["nisha","nancy","leo"], B=["121212121","111111111","444555666"] and P="112"
    # Expected output :
    NO MATCH 
    ```

    Link to solution [code](https://github.com/Valliammai-Subramanian/coding-questions-in-golang/tree/main/substring).