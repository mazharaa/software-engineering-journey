# Valid Anagram

Problems: [NeetCode](https://neetcode.io/problems/is-anagram/question?list=neetcode150)

## Problem

Given two strings `s` and `t`, return `true` if the two strings are anagrams of each other, otherwise return `false`.

An anagram is a string that contains the exact same characters as another string, but the order of the characters can be different.

Example 1:

```
Input: s = "racecar", t = "carrace"

Output: true
```

Example 2:

```
Input: s = "jar", t = "jam"

Output: false
```

Constraints:

- `1 <= s.length, t.length <= 5 \* 10^4`
- `s` and `t` consist of lowercase English letters.

## Approach

I use built-in map data structure from Go to solving this problem. the idea is comparing how many occurrence each character in both string. First step is compare both length, if not match diectly return `false`. Second create a map with `rune` as key and `int` as value then iterate through string for each char and store it to map, by incrementing the value by 1 for every looped char, fo that for the other string also. Third comparing each map value with the same map key. If the result is not match, return `false` directly otherwise return `true` after the iterated comparison is finished.

## Complxity

Time: O(n)

Space: O(k) where k is the number of distinct characters (worst case O(n)).

## Mistakes

I facing error while storing each char to map. It says `cannot use char (variable of type rune) as string value in map index`, that is because I use string for key data type instead of rune.

## Code

```go
func isAnagram(s string, t string) bool {
	if len(s) != len(t) {
		return false
	}

	smap := stringToMap(s)
	tmap := stringToMap(t)

	for _, char := range s {
		if smap[char] != tmap[char] {
			return false
		}
	}

	return true
}

func stringToMap(s string) map[rune]int {
	smap := make(map[rune]int)

	for _, char := range s {
		smap[char] += 1
	}

	return smap
}
```

## Review

Can I solve this without looking?

[] Yes

[v] No
