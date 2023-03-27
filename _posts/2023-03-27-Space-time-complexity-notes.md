---
toc: true
comments: false
layout: post
title: Space time complexity notes
description: Notes for the lesson space time complexity
permalink: /STCN
categories: [blog, lesson, notes] 
---

# Space and Time Complexity
> Space complexity refers to the amount of memory used by an algorithm to complete its execution, as a function of the size of the input. The space complexity of an algorithm can be affected by various factors such as the size of the input data, the data structures used in the algorithm, the number and size of temporary variables, and the recursion depth. Time complexity refers to the amount of time required by an algorithm to run as the input size grows. It is usually measured in terms of the "Big O" notation, which describes the upper bound of an algorithm's time complexity.


## > Why do you think a programmer should care about space and time complexity?

- is it a good idea to think about space and time complexity because time is important running a program and we don't want to waste it. 
- also we should use our memory efficiently because we have a limited amount.

## Volcano images

> Do you think this is a time complexity or space complexity or both problem? 
- it is a problem of both. it takes a long time because there is too much pixels to redner.

---

## Big O notation
there are multiple big O notation some being:
- Constant O(1)
- Linear O(n)
- Quadratic O(n^2) 
- Logarithmic O(logn)
- Exponential (O(2^n))

## Constant O(1)

### Time
> An example of a constant time algorithm is accessing a specific element in an array. It does not matter how large the array is, accessing an element in the array takes the same amount of time. Therefore, the time complexity of this operation is constant, denoted by O(1).

### Space
> This function takes two number inputs and returns their sum. The function does not create any additional data structures or variables that are dependent on the input size, so its space complexity is constant, or O(1). Regardless of how large the input numbers are, the function will always require the same amount of memory to execute.

## linear O(n)

### Time
> An example of a linear time algorithm is traversing a list or an array. When the size of the list or array increases, the time taken to traverse it also increases linearly with the size. Hence, the time complexity of this operation is O(n), where n is the size of the list or array being traversed.

### Space
> This function takes a list of elements arr as input and returns a new list with the elements in reverse order. The function creates a new list reversed_arr of the same size as arr to store the reversed elements. The size of reversed_arr depends on the size of the input arr, so the space complexity of this function is O(n). As the input size increases, the amount of memory required to execute the function also increases linearly.

## Quadratic O(n^2)

### Time
> An example of a quadratic time algorithm is nested loops. When there are two nested loops that both iterate over the same collection, the time taken to complete the algorithm grows quadratically with the size of the collection. Hence, the time complexity of this operation is O(n^2), where n is the size of the collection being iterated over.

### Space
> This function takes two matrices matrix1 and matrix2 as input and returns their product as a new matrix. The function creates a new matrix result with dimensions m by n to store the product of the input matrices. The size of result depends on the size of the input matrices, so the space complexity of this function is O(n^2). As the size of the input matrices increases, the amount of memory required to execute the function also increases quadratically.

## Logarithmic O(logn)

### Time
> An example of a log time algorithm is binary search. Binary search is an algorithm that searches for a specific element in a sorted list by repeatedly dividing the search interval in half. As a result, the time taken to complete the search grows logarithmically with the size of the list. Hence, the time complexity of this operation is O(log n), where n is the size of the list being searched.

### Space
> The same algorithm above has a O(logn) space complexity. The function takes an array arr, its lower and upper bounds low and high, and a target value target. The function searches for target within the bounds of arr by recursively dividing the search space in half until the target is found or the search space is empty. The function does not create any new data structures that depend on the size of arr. Instead, the function uses the call stack to keep track of the recursive calls. Since the maximum depth of the recursive calls is O(logn), where n is the size of arr, the space complexity of this function is O(logn). As the size of arr increases, the amount of memory required to execute the function grows logarithmically.

## Exponential O(2^n)

### Time
> An example of an O(2^n) algorithm is the recursive implementation of the Fibonacci sequence. The Fibonacci sequence is a series of numbers where each number is the sum of the two preceding ones, starting from 0 and 1. The recursive implementation of the Fibonacci sequence calculates each number by recursively calling itself with the two preceding numbers until it reaches the base case (i.e., the first or second number in the sequence). The algorithm takes O(2^n) time in the worst case because it has to calculate each number in the sequence by making two recursive calls.

### Space
> This function takes a set s as input and generates all possible subsets of s. The function does this by recursively generating the subsets of the set without the first element, and then adding the first element to each of those subsets to generate the subsets that include the first element. The function creates a new list for each recursive call that stores the subsets, and each element in the list is a new list that represents a subset. The number of subsets that can be generated from a set of size n is 2^n, so the space complexity of this function is O(2^n). As the size of the input set increases, the amount of memory required to execute the function grows exponentially.

> Using the time library, we are able to see the difference in time it takes to calculate the fibonacci function above.
- Based on what is known about the other time complexities, hypothesize the resulting elapsed time if the function is replaced. 

# Hacks
# Hacks
- Record your findings when testing the time elapsed of the different algorithms.
    - The time complexity is often expressed in big O notation, which gives an upper bound on the number of operations required as the input size grows. A lower time complexity is generally better, as it means the algorithm or operation is more efficient.
    - The space complexity is also often expressed in big O notation, and a lower space complexity is generally better.
    - Arrays have a constant time complexity for accessing an element by index (O(1)), but a linear time complexity for searching or inserting an element in an unsorted array (O(n)).
    - Linked lists have a constant time complexity for inserting or deleting an element at the beginning of the list (O(1)), but a linear time complexity for accessing or searching for an element in the list (O(n)).
    - The space complexity of a linked list is also proportional to the number of elements it contains (O(n)).

---


- Although we will go more in depth later, time complexity is a key concept that relates to the different sorting algorithms. Do some basic research on the different types of sorting algorithms and their time complexity.
    1. Bubble Sort:
        - Time complexity: O(n^2)
        - Space complexity: O(1)
        - Bubble sort is a simple sorting algorithm that repeatedly swaps adjacent elements if they are in the wrong order. It has a time complexity of O(n^2), making it inefficient for large datasets.

    2. Selection Sort:
        - Time complexity: O(n^2)
        - Space complexity: O(1)
        - Selection sort repeatedly finds the minimum element in an unsorted array and swaps it with the first element. It also has a time complexity of O(n^2).

    3. Insertion Sort:
        - Time complexity: O(n^2) for worst and average case, O(n) for best case.
        - Space complexity: O(1)
        - Insertion sort is a simple sorting algorithm that builds the final sorted array one item at a time. It has an average and worst-case time complexity of O(n^2), but a best-case time complexity of O(n) when the input array is already sorted.

    4.   Merge Sort:
        - Time complexity: O(n log n)
        - Space complexity: O(n)
        - Merge sort is a divide and conquer algorithm that recursively divides the input array in half, sorts each half, and then merges them back together. It has a time complexity of O(n log n), making it more efficient than the previous three algorithms for large datasets.

    5. Quick Sort:
        - Time complexity: O(n log n) for average case, O(n^2) for worst case.
        -  Space complexity: O(log n) for average case, O(n) for worst case.
        -  Quick sort is another divide and conquer algorithm that selects a pivot element, partitions the array around the pivot, and recursively sorts the two partitions. It has an average-case time    complexity of O(n log n), but a worst-case time complexity of O(n^2) when the input array is already sorted or mostly sorted.

---
       
- Why is time and space complexity important when choosing an algorithm?

    - Time and space complexity are important considerations when choosing an algorithm because they directly impact the performance and efficiency of the algorithm.

---

- Should you always use a constant time algorithm / Should you never use an exponential time algorithm? Explain? 
    - No, the choice of algorithm depends on the specific use case and requirements. Constant time algorithms are preferred for small input sizes and high performance requirements, while linear or even exponential time algorithms may be necessary for larger input sizes. Exponential time algorithms should generally be avoided due to their extremely slow performance for larger input sizes, but there may be certain use cases where they are the only viable option. Ultimately, it's important to consider both time and space complexity when choosing an algorithm, as they directly impact the performance and efficiency of the algorithm. The goal is to choose the algorithm that provides the best balance of performance and efficiency for the specific use case and input data.

---

- What are some general patterns that you noticed to determine each algorithm's time and space complexity?
    - Looping
    - Recursion
    - Nested loops
    - Divide and conquer
    - Sorting
    - Data structure


Complete the Time and Space Complexity analysis questions linked below.
[Practice](https://www.geeksforgeeks.org/practice-questions-time-complexity-analysis/)
# Q & A


## 1
```python

int a = 0, b = 0;
for (i = 0; i < N; i++) {
    a = a + rand();
}
for (j = 0; j < M; j++) {
    b = b + rand();
}
```

1. O(N * M) time, O(1) space
2. O(N + M) time, O(N + M) space

3. <mark>O(N + M) time, O(1) space<mark>

4. O(N * M) time, O(N + M) space

the correct answer is #3, N and M are independent variables

## 2
```python

int a = 0;
for (i = 0; i < N; i++) {
    for (j = N; j > i; j--) {
        a = a + i + j;
    }
}
```

1. O(N)
2. O(N*log(N))
3. O(N * Sqrt(N))
4. <mark> O(N*N) </mark>

the code above does not run

## 3
```python

int i, j, k = 0;
for (i = n / 2; i <= n; i++) {
    for (j = 2; j <= n; j = j * 2) {
        k = k + n / 2;
    }
}
```

1. O(n)
2. <mark> O(N log N) </mark>
3. O(n^2)
4. O(n^2Logn)

j keeps doubling but it is still less than one
## 4

```python
 What does it mean when we say that an algorithm X is asymptotically more efficient than Y? 
```

1. X will always be a better choice for small inputs
2. <mark> X will always be a better choice for large inputs </mark>
3. Y will always be a better choice for small inputs
4. X will always be a better choice for all inputs

Asymptotic analysis compares algorithms based on their performance as input size approaches infinity

## 5
```python
int a = 0, i = N;
while (i > 0) {
    a += i;
    i /= 2;
}
```
1. O(N)
2. O(Sqrt(N))
3. O(N / 2)
4. <mark> O(log N) </mark>

We have to find the smallest x such that ‘(N / 2^x )< 1 OR  2^x > N’ 
x = log(N)

## 6 
```python
Which of the following best describes the useful criterion for comparing the efficiency of algorithms?
```

1. Time
2. Memory
3. <mark> Both of the above </mark>
4. None of the above

common sense

## 7
```python
How is time complexity measured?
```
1. By counting the number of algorithms in an algorithm.
2. <mark> By counting the number of primitive operations performed by the algorithm on a given input size. </mark>
3. By counting the size of data input to the algorithm.
4. None of the above



## 8
```python
for(var i=0;i<n;i++)
    i*=k
```
1. O(n)
2. O(k)
3. <mark> O(logkn) </mark>
4. O(lognk)

Because loops for the kn-1 times, so after taking log it becomes logkn.

## 9
```python
int value = 0;
for(int i=0;i<n;i++)
    for(int j=0;j<i;j++)
      value += 1;
```

1. n
2. (n+1)
3. <mark> n(n-1) </mark>
4. n(n+1)

 First for loop will run for (n) times and another for loop will be run for (n-1) times as the inner loop will only run till the range i which is 1 less than n , so overall time will be n(n-1).

## 10
```python
Algorithm A and B have a worst-case running time of O(n) and O(logn), respectively. Therefore, algorithm B always runs faster than algorithm A.
```

1. True
2. <mark> False </mark>


The Big-O notation provides an asymptotic comparison in the running time of algorithms. For n < n0​​, algorithm A might run faster than algorithm B, for instance.



# big idea 2
note: need vpn to view these images on school wifi. 
![image](https://media.discordapp.net/attachments/914072417310232616/1087593110370013244/bigidea2.png?width=1683&height=187)