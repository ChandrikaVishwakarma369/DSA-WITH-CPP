# DSA-WITH-CPP

This repository contains C++ implementations of common data structures and algorithms problems, organized by topic (e.g., Array, String).

## Array/twoSum_SortedInput.cpp

Solves the Two Sum problem assuming the input array is sorted in non-decreasing order.

### Problem Description
Given an array of integers `numbers` sorted in ascending order and a target value `target`, return the **1-based indices** of the two numbers such that they add up to the target. You may assume that there is exactly one solution, and you may not use the same element twice.

### Approach
A **two-pointer technique** is used:
1. Initialize two pointers, one at the start (`i`) and one at the end (`j`) of the array.
2. While `i < j`:
   * Compute the sum of `numbers[i] + numbers[j]`.
   * If the sum equals the target, return the pair of indices `(i+1, j+1)`.
   * If the sum is less than the target, increment `i` to increase the sum.
   * If the sum is greater than the target, decrement `j` to decrease the sum.
3. If no pair is found, return an empty vector (though the problem guarantees one solution).

### Example
Input: numbers = {2, 7, 11, 15}, target = 9
Output: 1 2 (since numbers[0] + numbers[1] = 2 + 7 = 9)

The code is implemented in `Array/twoSum_SortedInput.cpp` and demonstrates the two-pointer solution in the `twoSum` function.
