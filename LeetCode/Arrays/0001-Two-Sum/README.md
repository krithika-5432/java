# [1. Two Sum](https://leetcode.com/problems/two-sum/)

## Problem Statement

Given an array of integers `nums` and an integer `target`, return the **indices of the two numbers** such that they add up to `target`.

You may assume that each input has **exactly one solution**, and you may not use the same element twice.

You can return the answer in any order.

## Example 1

**Input:** `nums = [2,7,11,15], target = 9`

**Output:** `[0,1]`

**Explanation:** `nums[0] + nums[1] = 2 + 7 = 9`

## Example 2

**Input:** `nums = [3,2,4], target = 6`

**Output:** `[1,2]`

## Example 3

**Input:** `nums = [3,3], target = 6`

**Output:** `[0,1]`

## Constraints

- `2 <= nums.length <= 10^4`
- `-10^9 <= nums[i] <= 10^9`
- `-10^9 <= target <= 10^9`
- Only one valid answer exists.

## Approach

Use two nested loops to check every possible pair of elements.

- The first loop selects an element using index `i`.
- The second loop selects the next element using index `j`.
- Check whether `nums[i] + nums[j]` equals the target.
- If the sum equals the target, return the indices `i` and `j`.

## Complexity Analysis

**Time Complexity:** `O(n²)`

Two nested loops are used, so every possible pair may be checked in the worst case.

**Space Complexity:** `O(1)`

No extra data structure is used.

## LeetCode Performance

- **Runtime:** 45 ms
- **Beats:** 26.94%
- **Memory:** 47.23 MB
- **Beats:** 23.81%