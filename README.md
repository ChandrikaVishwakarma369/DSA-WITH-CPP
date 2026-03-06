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

## Array/3sum.cpp

Solves the 3Sum problem from LeetCode.

### Problem Description
Given an integer array `nums`, return all the triplets `[nums[i], nums[j], nums[k]]` such that `i != j`, `i != k`, and `j != k`, and `nums[i] + nums[j] + nums[k] == 0`.

Notice that the solution set must not contain duplicate triplets.

### Approach
The solution uses a **sorting and two-pointer technique**:
1. Sort the input array.
2. Iterate through the array with the first pointer `i` from 0 to n-3.
3. For each `i`, use two pointers `left` and `right` to find pairs that sum to `-nums[i]`.
4. Skip duplicates for `i`, `left`, and `right` to avoid duplicate triplets.
5. If the sum of `nums[left] + nums[right]` equals the target, add the triplet and move both pointers.
6. If less, move `left` right; if more, move `right` left.

### Example
Input: nums = [-1,0,1,2,-1,-4]
Output: [[-1,-1,2],[-1,0,1]]

The code is implemented in `Array/3sum.cpp` and demonstrates the sorting and two-pointer solution in the `threeSum` function.
