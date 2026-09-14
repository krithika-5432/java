# [189. Rotate Array](https://leetcode.com/problems/rotate-array/)

## Problem Statement

Given an integer array `nums`, rotate the array to the **right by `k` steps**, where `k` is non-negative.

## Example 1

**Input:** `nums = [1,2,3,4,5,6,7], k = 3`

**Output:** `[5,6,7,1,2,3,4]`

**Explanation:**  
After rotating the array 3 steps to the right, the last three elements move to the beginning.

## Example 2

**Input:** `nums = [-1,-100,3,99], k = 2`

**Output:** `[3,99,-1,-100]`

**Explanation:**  
After rotating the array 2 steps to the right, `3` and `99` move to the beginning.

## Constraints

- `1 <= nums.length <= 10^5`
- `-2^31 <= nums[i] <= 2^31 - 1`
- `0 <= k <= 10^5`

## Approach

Use the **Array Reversal** technique to rotate the array in-place.

- First, calculate `k % n` to handle cases where `k` is greater than the array length.
- Reverse the entire array.
- Reverse the first `k` elements.
- Reverse the remaining `n - k` elements.
- This places the last `k` elements at the beginning while keeping their original order.

## Complexity Analysis

**Time Complexity:** `O(n)`

The array is reversed three times, and each reversal takes linear time.

**Space Complexity:** `O(1)`

The rotation is performed in-place without using an extra array.