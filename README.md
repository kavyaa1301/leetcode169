# leetcode169
Approach :
This solution leverages a key property of the majority element: if an element appears more than ⌊n / 2⌋ times in a sorted array, it must occupy the middle position.


Intuition :
Imagine lining up all the elements in sorted order. The majority element, by definition, accounts for more than half of the array's length. Therefore, no matter how the other elements are distributed, the central element in the sorted list (at index n/2) is guaranteed to be the majority element.


Example:
Array: [2, 2, 1, 1, 1, 2, 2]
Sorted: [1, 1, 1, 2, 2, 2, 2]
Length n = 7, so middle index is 7 / 2 = 3 (0-based indexing).
The element at index 3 is 2, which is the correct majority element.


Algorithm :
Sort the input array nums in non-decreasing order.
Return the element located at the index n/2, where n is the length of the array.


Complexity Analysis :
Time Complexity: O(n log n)
The dominant operation is sorting the array. The time complexity of efficient sorting algorithms (like Quicksort, Mergesort, or Heapsort, which are used by C++'s std::sort) is O(n log n).
Space Complexity: O(1) or O(n)
O(1): If the sorting algorithm is performed in-place and doesn't use significant additional space (e.g., Heapsort).
O(log n) or O(n): Depending on the sorting algorithm implementation used by the language's standard library. For example, std::sort in C++ is typically a hybrid sort (like Introsort) that has a O(log n) stack space complexity for recursion.

Conclusion:
The sorting solution is an elegant and intuitive way to solve the Majority Element problem. While it is not the most asymptotically efficient algorithm, its simplicity makes it an excellent choice for quick implementation, especially in contexts where the input size is not extremely large or where code clarity is paramount. For the absolute best performance, the Boyer-Moore Voting Algorithm is preferred.

