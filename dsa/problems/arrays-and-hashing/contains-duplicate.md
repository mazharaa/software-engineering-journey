# Contains Duplicate

Reference: [NeetCode](https://neetcode.io/problems/duplicate-integer/question?list=neetcode150)

## Problem

Given an integer array `nums`, return `true` if any value appears more than once in the array, otherwise return `false`.

## Pattern

`Array` `Hash Table` `Sorting`

## Approach

At my first approach I use built-in sorting method to sort the array first, then I iterate through the array to check every element if the current element has same value with the next element.

My second approach is using map/hash table. At first I declare the map variable, then I iterate through the array and add each element to map/hash table as key and the appearance as value. If the value > 1 directly return true, but if there is no value > 1 along iteration then return false.

My third approach is quite same from my second approach. Instead count each element appearance, I use bool as map value. So if the element is already added to the map/hash table it will directly return true, if there is no then return false

## Complexity

- First Aproach
  Time: O(n log n)
  Space: O(log n)

- Second Approach
  Time: O(n)
  Space: O(n)

- Second Approach
  Time: O(n)
  Space: O(n)

## Mistakes

-

## Code

- First approach, sort first

  ```go
  import "slices"
  func hasDuplicate(nums []int) bool {
  slices.Sort(nums)

    for i := 0; i < len(nums) - 1; i ++ {
        if nums[i] == nums[i+1] {
            return true
        }
    }

    return false
  }
  ```

  ```python
  class Solution:
    def hasDuplicate(self, nums: List[int]) -> bool:
        nums.sort()

        for i in range(len(nums) - 1):
            if nums[i] == nums[i + 1]:
                return True

        return False
  ```

  ```java
  class Solution {
    public boolean hasDuplicate(int[] nums) {
        Arrays.sort(nums);

        for(int i = 0; i < nums.length - 1; i ++) {
            if (nums[i] == nums[i + 1]) {
                return true;
            }
        }

        return false;
    }
  }
  ```

- Second approach, map with counter

  ```go
  func hasDuplicate(nums []int) bool {
    m := make(map[int]int)

    for _, value := range nums {
        m[value] ++

        if m[value] > 1 {
            return true
        }
    }
    return false
  }
  ```

  ```python
  class Solution:
    def hasDuplicate(self, nums: List[int]) -> bool:
        h = {}

        for num in nums:
            h[num] = h.get(num, 0) + 1

            if h[num] > 1:
                return True

        return False
  ```

  ```java
  class Solution {
    public boolean hasDuplicate(int[] nums) {
        Map<Integer, Integer> m = new HashMap<>();

        for(int num : nums) {
            m.merge(num, 1, Integer::sum);

            if(m.get(num) > 1) {
                return true;
            }
        }

        return false;
    }
  }
  ```

- Third approach, map with boolean value

  ```go
  func hasDuplicate(nums []int) bool {
    m := make(map[int]bool)

    for _, value := range nums {
        if m[value] {
            return true
        }
        m[value] = true
    }

    return false
  }
  ```

  ```python
  class Solution:
    def hasDuplicate(self, nums: List[int]) -> bool:
        s = set()

        for num in nums:
            if num in s:
                return True

            s.add(num)

        return False
  ```

  ```java
  class Solution {
    public boolean hasDuplicate(int[] nums) {
        HashSet<Integer> h = new HashSet<>();

        for(int num : nums) {
            if(!h.add(num)) {
                return true;
            }

            h.add(num);
        }

        return false;
    }
  }
  ```

## Review

Can I solve this without looking?

- [ v ] Yes
- [ ] No
