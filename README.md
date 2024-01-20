# C - Sorting algorithms &amp; Big O project
##### C, Algorithm, Data structure


## Background Context Resources
This project is meant to be done by groups of two students. Each group of two should pair program for at least the mandatory part.

### Read or watch:

1. Sorting algorithm
2. Big O notation
3. Sorting algorithms animations
4. __15 sorting algorithms in 6 minutes__ (WARNING: The following video can trigger seizure/epilepsy. It is not required for the project, as it is only a funny visualization of different sorting algorithms)
5. CS50 Algorithms explanation in detail by David Malan
6. All about sorting algorithms


## General Learning Objectives
At the end of this project, you are expected to be able to *explain to anyone*, without the help of Google:

* At least four different sorting algorithms
* What is the Big O notation, and how to evaluate the time complexity of an algorithm
* How to select the best sorting algorithm for a given input
* What is a stable sorting algorithm


## General Requirements

1. Allowed editors: vi, vim, emacs
2. All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
3. All your files should end with a new line
4. A README.md file, at the root of the folder of the project, is mandatory
5. Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
6. You are not allowed to use global variables
7. No more than 5 functions per file
8. Unless specified otherwise, you are not allowed to use the standard library. Any use of functions like printf, puts, … is totally forbidden.
9. In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
10. The prototypes of all your functions should be included in your header file called sort.h
11. Don’t forget to push your header file
12. All your header files should be include guarded
13. A list/array does not need to be sorted if its size is less than 2.

## More Data Structure and Functions Info

For this project you are given the following *print_array*, and *print_list* functions:

----------------------------------------------------------------------------------------------------------------
#include <stdlib.h>
#include <stdio.h>

/**
 * print_array - Prints an array of integers
 *
 * @array: The array to be printed
 * @size: Number of elements in @array
 */
void print_array(const int *array, size_t size)
{
    size_t i;

    i = 0;
    while (array && i < size)
    {
        if (i > 0)
            printf(", ");
        printf("%d", array[i]);
        ++i;
    }
    printf("\n");
}

-------------------------------------------------------------------------------------------------------------------------------------------
#include <stdio.h>
#include "sort.h"

/**
 * print_list - Prints a list of integers
 *
 * @list: The list to be printed
 */
void print_list(const listint_t *list)
{
    int i;

    i = 0;
    while (list)
    {
        if (i > 0)
            printf(", ");
        printf("%d", list->n);
        ++i;
        list = list->next;
    }
    printf("\n");
}

* Our files __print_array.c__ and __print_list.c__ (containing the __print_array.c__ and __print_list.c__ functions) will be compiled with your functions during the correction.
* Please declare the prototype of the functions __print_array__ and __print_list__ in your __sort.h__ header file
* Please use the following data structure for doubly linked list:

--------------------------------------------------------------------------------------------------------------------------------
/**
 * struct listint_s - Doubly linked list node
 *
 * @n: Integer stored in the node
 * @prev: Pointer to the previous element of the list
 * @next: Pointer to the next element of the list
 */
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;

Please, note this format is used for Quiz and Task questions.

1. O(1)
2. O(n)
3. O(n!)
4. n square -> O(n^2)
5. log(n) -> O(log(n))
6. n * log(n) -> O(nlog(n))
7. n + k -> O(n+k) …

Please use the “short” notation (don’t use constants). Example: *O(nk)* or *O(wn)* should be written *O(n)*. If an answer is required within a file, all your answers files must have a newline at the end.

Tests
Here is a quick tip to help you test your sorting algorithms with big sets of random integers: Random.org

## Copyright - Plagiarism
1. You are tasked to come up with solutions for the tasks below yourself to meet with the above learning objectives.
2. You will not be able to meet the objectives of this or any following project by copying and pasting someone else’s work.
3. You are not allowed to publish any content of this project.
4. Any form of plagiarism is strictly forbidden and will result in removal from the program.

# GitHub Rule
There should be one project repository per group. If you clone/fork/whatever a project repository with the same name before the second deadline, you risk a 0% score.


*C - Sorting algorithms &amp; Big O project by Benny &amp; Danny*
