# Problem Solving Patterns

---
## Frequency counter

Uses objects to set/collect values or the frequency of values.

This often avoids the need for nested loops or n squared operations.

Remember that two nested loops are far worse than two separate loops.

This pattern usually involves dictionaries/objects that count frequencies.

Iterate over objects in separate loops and adjust/compare frequencies of values.

---
## Multiple pointers

Creating pointers that correspond to an index/position and move towards each other at the beginning, middle, or end based on a certain condition.

Very efficient with minimal space complexity as well.

---
## Sliding window

Create a window which can either be an array or a number from one position to another.

The window either increases or closes depending on the conditions

Very useful for keeping track of a subset of data in an array/string etc.

The window can be a single variable, sub array, or even a string.

Usually move from left to right.

---
## Divide and conquer

Involves dividing a data set into smaler chunks and then repeating a process with a subset of data.

This pattern can tremendously decrease time complexity.

e.g. Binary Search/Mergesort