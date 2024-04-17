# Leet 242. Valid Anagram

:green_square: Easy

Given two strings `s` and `t`, return true if `t` is an anagram of `s`, and false otherwise.

An Anagram is a word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once.

### Example 1:

**Input:**
s = "anagram", t = "nagaram"

**Output:**
true

### Example 2:

**Input:**
s = "rat", t = "car"

**Output:**
false

### Constraints:

- 1 <= s.length, t.length <= 5 \* 10^4
- `s` and `t` consist of lowercase English letters.

### Solution:

```Java
class Solution {
    public boolean isAnagram(String s, String t) {
        //Let check if both string length match
        if(s.length() != t.length()){
            return true;
        }

        char[] sCharArray = s.toCharArray();
        char[] tCharArray = t.toCharArray();

        Arrays.sort(sCharArray);
        Arrays.sort(tCharArray);

        return Arrays.equals(sCharArray, tCharArray);
    }
}
```
