# Leetcode-1460.-Make-Two-Arrays-Equal-by-Reversing-Subarrays
# Description
You are given two integer arrays of equal length target and arr. In one step, you can select any non-empty subarray of arr and reverse it. You are allowed to make any number of steps.

Return true if you can make arr equal to target or false otherwise.

# Solution
You can reverse any subarray any number of times, so you can basically rearrange arr in any way you want.

So, the problem reduces to:
➡️ Can we rearrange arr to match target?

Example ;
Input: target = [1,2,3,4], arr = [2,4,1,3]

Output: true

Explanation: You can follow the next steps to convert arr to target

1- Reverse subarray [2,4,1], arr becomes [1,4,2,3]


2- Reverse subarray [4,2], arr becomes [1,2,4,3]

3- Reverse subarray [4,3], arr becomes [1,2,3,4

There are multiple ways to convert arr to target, this is not the only way to do so.

That’s true if and only if both arrays contain the same elements with the same frequencies.
# Algorithm
1. sort both target and arr.
2. If the sorted arrays are equal, return True; otherwise, return False.
# Code
class Solution:

    def canBeEqual(self, target: List[int], arr: List[int]) -> bool:
        return sorted(arr)==sorted(target)
# Complexity
 Time Complexity: O(n log n)
 
Sorting arr takes O(n log n)

Sorting target takes O(n log n)

Comparing the two arrays takes O(n)

Total: O(n log n)

Space Complexity: O(n)

Sorting creates new arrays, not in-place (in Python), so space = O(n)

No additional data structures used

