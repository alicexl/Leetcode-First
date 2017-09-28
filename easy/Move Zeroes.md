## 283. Move Zeroes
Given an array ```nums```, write a function to move all ```0```'s to the end of it while maintaining the relative order of the non-zero elements.

For example, given ```nums = [0, 1, 0, 3, 12]```, after calling your function, ```nums``` should be ```[1, 3, 12, 0, 0]```.

###Note:
1. You must do this in-place without making a copy of the array.
2. Minimize the total number of operations.

###一刷
1. 不能用切片，引用传递，需要直接修改某个nums[index]
2. 通过每发现0,然后移位的方法完成一波，时间复杂度O(0的个数*n)
3. 只循环一遍的方法需要记住0的个数，结束条件为i > length - 1 - zero_cnt，如果发现有0，则找到下一个不为0的数，然后只赋当前i为 i+zero_cnt; 时间复杂度为O(n + 0的个数)