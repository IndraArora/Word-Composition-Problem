# Steps to Execution

### 1. Compile the Code

bash
g++ -o comp_word_prog comp_word.cpp

### 2. Prepare Input File:

Ensure that the input file "Input_01.txt"/"Input_02.txt" containing the list of words is available in the same directory as the compiled program.

### 3. Run the Program:

bash
./comp_word_prog

### 4. View Output:

The program will output the longest and second longest compounded words along with the execution time.

# Overview

The provided C++ program aims to identify and display the longest and second-longest compounded words from a list of words stored in a file. Compounded words are defined as those that can be constructed by combining two or more shorter words from the given list. The program employs a sorting-based approach along with dynamic programming concepts, including the implementation of a Trie data structure, to efficiently identify compounded words.

# Approach

1. _File Input_: The program reads the list of words from an input file named Input_01.txt \ Input_02.txt.

2. _Sorting by Length_:
   To efficiently find compounded words, the list of words is sorted based on their length in ascending order. This allows for easier detection of smaller words within longer ones.

3. _Finding Compounded Words_:
   For each word in the sorted list, the program iterates through its characters to check for compounded words.
   Utilizing the Trie, the program validates the existence of shorter words in the list. If a valid splitting point is found, the word is marked as compounded and added to the
   list of compounded words.

4. _Output Processing_:

- The compounded words are sorted based on their lengths.
- The longest and second longest compounded words are displayed.
- The execution time of the code is also provided.

# Design Decisions:

1. _Comparator Function_:
   A comparator function sorts the words based on their lengths. This ensures that shorter words are considered first during the compounded word search, potentially improving efficiency.

2. _Data Structures_:
   The program employs maps, sets, and a vector data structure to efficiently store and retrieve information about encountered words, split points, and validate the existence of shorter words.

3. _Input/Output Optimization_:
   The program optimizes input/output performance by utilizing ios_base::sync_with_stdio(false) and cin.tie(NULL).

# Code Flow Diagram

1. Start

│
▼ 2. Read Input from File
│
▼ 3. Sort Words by Length
│
▼ 4. Initialize Trie Data Structure
│
▼ 5. For each word in sorted list:
│
├─── Check if word is compounded:
│ │
│ ▼
│ Iterate over word characters
│ │
│ ├─── Check if current prefix is in Trie:
│ │ │
│ │ ├─── If yes, check if remaining part is in Trie:
│ │ │ │
│ │ │ ├─── If yes, mark as compounded
│ │ │ │
│ │ │ └─── If no, continue
│ │ │
│ │ └─── If no, continue
│ │
│ └─── Update Trie with current word
│
└─── Update Trie with current word

6. Sort Compounded Words by Length
   │
   ▼
7. Print Longest and Second Longest Compounded Words
   │
   ▼
8. Print Time Taken by Code

9. End
