# [162. Find Peak Element](https://leetcode.com/problems/find-peak-element/)

## Problem Statement

Given a **0-indexed** integer array `nums`, find a peak element and return its index.

A peak element is an element that is **strictly greater than its neighbors**.

If the array contains multiple peaks, you can return the index of **any peak**.

You may assume that elements outside the array have a value of negative infinity.

The algorithm must run in `O(log n)` time.

## Example 1

**Input:** `nums = [1,2,3,1]`

**Output:** `2`

**Explanation:** `3` is greater than both its neighbors, so index `2` is a peak.

## Example 2

**Input:** `nums = [1,2,1,3,5,6,4]`

**Output:** `5`

**Explanation:** `6` is greater than both its neighbors, so index `5` is a peak. Index `1` would also be a valid answer.

## Constraints

- `1 <= nums.length <= 1000`
- `-2^31 <= nums[i] <= 2^31 - 1`
- `nums[i] != nums[i + 1]` for all valid `i`

## Approach

Use **Binary Search** to find a peak element.

- Set `low = 0` and `high = nums.length - 1`.
- Find the middle index `mid`.
- Compare `nums[mid]` with `nums[mid + 1]`.
- If `nums[mid] < nums[mid + 1]`, a peak must exist on the right side, so move `low` to `mid + 1`.
- Otherwise, a peak exists at `mid` or on the left side, so move `high` to `mid`.
- Continue until `low` and `high` become equal.
- Return `low` as the index of a peak element.

## Complexity Analysis

**Time Complexity:** `O(log n)`

Binary search reduces the search range by half in every iteration.

**Space Complexity:** `O(1)`

Only a constant amount of extra space is used.