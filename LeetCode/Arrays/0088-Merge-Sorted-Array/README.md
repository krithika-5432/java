# [88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)

## Problem Statement

You are given two integer arrays `nums1` and `nums2`, sorted in **non-decreasing order**, and two integers `m` and `n`.

Merge `nums1` and `nums2` into a single array sorted in **non-decreasing order**.

The merged array must be stored inside `nums1`.

The first `m` elements of `nums1` contain valid elements, while the last `n` elements are empty spaces represented by `0`.

## Example 1

**Input:** `nums1 = [1,2,3,0,0,0], m = 3, nums2 = [2,5,6], n = 3`

**Output:** `[1,2,2,3,5,6]`

**Explanation:**  
The arrays being merged are `[1,2,3]` and `[2,5,6]`. The merged array is `[1,2,2,3,5,6]`.

## Example 2

**Input:** `nums1 = [1], m = 1, nums2 = [], n = 0`

**Output:** `[1]`

**Explanation:**  
There are no elements to merge from `nums2`.

## Example 3

**Input:** `nums1 = [0], m = 0, nums2 = [1], n = 1`

**Output:** `[1]`

**Explanation:**  
`nums1` contains no valid elements, so the element from `nums2` is placed into `nums1`.

## Constraints

- `nums1.length == m + n`
- `nums2.length == n`
- `0 <= m, n <= 200`
- `1 <= m + n <= 200`
- `-10^9 <= nums1[i], nums2[j] <= 10^9`

## Approach

Use **Three Pointers** and merge the arrays from the end.

- Set `i` to the last valid element of `nums1`.
- Set `j` to the last element of `nums2`.
- Set `k` to the last position of `nums1`.
- Compare `nums1[i]` and `nums2[j]`.
- Place the larger element at position `k`.
- Move the corresponding pointer backward.
- Continue until all elements of `nums2` are merged.
- Merging from the end prevents overwriting the valid elements already present in `nums1`.

## Complexity Analysis

**Time Complexity:** `O(m + n)`

Each element is processed at most once.

**Space Complexity:** `O(1)`

The merging is performed directly inside `nums1` without using an extra array.