## 242. Valid Anagram ##
Given two strings s and t, write a function to determine if t is an anagram of s.

For example, 

s = "anagram", t = "nagaram", return true.

s = "rat", t = "car", return false.

### Note: ###
You may assume the string contains only lowercase alphabets.

###Follow up: ###
What if the inputs contain unicode characters? How would you adapt your solution to such case?

### 一刷
1. 和Find the Difference一样，可以在2*O(s)内完成
2. 最小O(1)
3. dict[key] ++    dict[key]--  方式去对每个key计数,最后存在key的value不为0,则不相等，在Find the Diffence里面，就转化成找到value不为0的那个key