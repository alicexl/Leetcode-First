## 665. Non-decreasing Array
Given an array with `n` integers, your task is to check if it could become non-decreasing by modifying **at most** `1` element.

We define an array is non-decreasing if `array[i] <= array[i + 1]` holds for every i (1 <= i < n).

### Example 1: ###
    Input: [4,2,3]
    Output: True
    Explanation: You could modify the first 
     4
     to 
     1
     to get a non-decreasing array.

### Example 2: ###
    Input: [4,2,1]
    Output: False
    Explanation: You can't get a non-decreasing array by modify at most one element.

###Note: ###
The `n` belongs to [1, 10,000].


### 一刷
1. 逆序对需要计数，超过一次即为False 
2. 结束条件要注意
3. 发现逆序对时，判断是否能fix，a b c d ，如果b c为逆序对，可以通过fix b，a b' c d;也可以fix c, a b c' d.有两种方案
4. False条件  逆序对 > 1  or 不可fix