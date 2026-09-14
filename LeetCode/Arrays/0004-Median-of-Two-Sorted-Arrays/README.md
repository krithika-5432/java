# [4. Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)

## Problem Statement

Given two sorted arrays `nums1` and `nums2` of size `m` and `n` respectively, return the **median** of the two sorted arrays.

The overall run time complexity should be `O(log(m + n))`.

## Example 1

**Input:**  
`nums1 = [1,3], nums2 = [2]`

**Output:**  
`2.00000`

**Explanation:**  
The merged array is `[1,2,3]` and the median is `2`.

## Example 2

**Input:**  
`nums1 = [1,2], nums2 = [3,4]`

**Output:**  
`2.50000`

**Explanation:**  
The merged array is `[1,2,3,4]` and the median is `(2 + 3) / 2 = 2.5`.

## Constraints

- `nums1.length == m`
- `nums2.length == n`
- `0 <= m <= 1000`
- `0 <= n <= 1000`
- `1 <= m + n <= 2000`
- `-10^6 <= nums1[i], nums2[i] <= 10^6`

## Approach

Use **Binary Search** to find the correct partition between the two sorted arrays.

The arrays are divided into left and right parts such that:

- Every element on the left side is less than or equal to every element on the right side.
- The left and right partitions contain the correct number of elements.
- The median can then be calculated from the boundary elements.

To achieve the required `O(log(m + n))` complexity, binary search is performed on the smaller array.

## Complexity Analysis

**Time Complexity:** `O(log(min(m, n)))`

Binary search is performed on the smaller array.

**Space Complexity:** `O(1)`

Only a constant amount of extra space is used.