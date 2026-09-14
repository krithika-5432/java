# [118. Pascal's Triangle](https://leetcode.com/problems/pascals-triangle/)

## Problem Statement

Given an integer `numRows`, return the first `numRows` of **Pascal's Triangle**.

In Pascal's Triangle, each number is the sum of the two numbers directly above it.

## Example 1

**Input:** `numRows = 5`

**Output:** `[[1],[1,1],[1,2,1],[1,3,3,1],[1,4,6,4,1]]`

**Explanation:**  
Each row starts and ends with `1`. The middle elements are calculated by adding the two numbers directly above them.

## Example 2

**Input:** `numRows = 1`

**Output:** `[[1]]`

## Constraints

- `1 <= numRows <= 30`

## Approach

Use nested loops to build each row of Pascal's Triangle.

- Create an empty list to store all the rows.
- For each row, create a new list.
- The first and last elements of every row are `1`.
- For the middle elements, add the two elements directly above them from the previous row.
- Add the completed row to the result.
- Continue until `numRows` rows are created.

## Complexity Analysis

**Time Complexity:** `O(n²)`

There are `n` rows, and the total number of elements generated is proportional to `n²`.

**Space Complexity:** `O(n²)`

The result contains all the elements of Pascal's Triangle.