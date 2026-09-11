# [26. Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)

## Problem Statement

Given an integer array `nums` sorted in **non-decreasing order**, remove the duplicates **in-place** so that each unique element appears only once.

Return the number of unique elements `k`.

The first `k` elements of `nums` should contain the unique numbers in sorted order. The elements beyond index `k - 1` can be ignored.

## Example 1

**Input:** `nums = [1,1,2]`

**Output:** `2, nums = [1,2,_]`

**Explanation:**  
The unique elements are `1` and `2`, so `k = 2`.

## Example 2

**Input:** `nums = [0,0,1,1,1,2,2,3,3,4]`

**Output:** `5, nums = [0,1,2,3,4,_,_,_,_,_]`

**Explanation:**  
The unique elements are `0, 1, 2, 3, and 4`, so `k = 5`.

## Constraints

- `1 <= nums.length <= 3 * 10^4`
- `-100 <= nums[i] <= 100`
- `nums` is sorted in **non-decreasing order**

## Approach

Use the **Two Pointer** technique.

- Use `i` to track the position of the last unique element.
- Use `j` to scan the array from the second element.
- If `nums[j]` is different from `nums[i]`, move `i` forward and place `nums[j]` at `nums[i]`.
- Continue until the entire array is checked.
- Return `i + 1` as the number of unique elements.

## Complexity Analysis

**Time Complexity:** `O(n)`

The array is traversed only once using the two pointers.

**Space Complexity:** `O(1)`

The duplicates are removed in-place without using any extra data structure.

## LeetCode Performance

- **Runtime:** 0 ms
- **Beats:** 100.00%
- **Memory:** 47.03 MB
- **Beats:** 9.04%