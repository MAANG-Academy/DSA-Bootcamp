# DSA-Bootcamp


## Course Structure

| No. | Topic. | Week
| ---|---|---
| 1. | DSA Level I | 1-10
| 2. | Mock Interviews | 11
| 3. | DSA Level II. Curated list of problems | 12-21
| 4. | Mock Interviews | 22,25
| 5. | Low Level Design, Design patterns | 23-24



## 1. DSA Level I

Platform: https://leetcode.com/explore/learn/

| No. | Topic. | Week
| ---|---|---
| 1. | [Arrays](#1-arrays)  | 1
| 2. | Arrays & Strings | 1
| 3. | Hash Table | 2
| 4. | Stack & Queue  | 2
| 5. | Heap | 3
| 6. | Linked List  | 3
| 7. | Binary Tree  | 4
| 8. | Recursion I  | 4
| 9. | Recursion II | 4
| 10. | Binary Search | 5
| 11. | Binary Search Tree  | 5
| 12. | Dynamic Programming | 6,7
| 13. | Graph | 7,8
| 14. | Nary Tree | 9
| 15. | Trie  | 9
| 16. | Segment Tree, Fenwick Tree  | 10
| 17. | Sliding Window  | 10
| 18. | Math, Misc, Catalan Numbers,Bit manipulation etc  | 10


## 1. Arrays 

Complete this module in 3 days : https://leetcode.com/explore/learn/card/fun-with-arrays/. The solutions are given below.

1. [Max Consecutive Ones](https://leetcode.com/problems/max-consecutive-ones/)

```c++
int findMaxConsecutiveOnes(vector<int>& nums) {
        int ans=0,cur=0;
        for (const auto& i:nums){
           if (i==1)
                ans=max(ans,++cur);
           else cur=0;
        }
        return ans;
    }
```
Time Complexity : O(n)\
Space Complexity : O(1)


2. [Find Numbers with Even Number of Digits](https://leetcode.com/problems/find-numbers-with-even-number-of-digits/)

```cpp
    int findNumbers(vector<int>& nums) {
        int ans=0,count=0;
        for (auto& num:nums)
        {
            count=0;
            while(num) {
                count++;
                num/=10;
            }
            if (count%2==0) ans++;
        }
        return ans;
    }
```
    
Time Complexity : O(n)\
Space Complexity : O(1)

3. [Squares of a Sorted Array](https://leetcode.com/problems/squares-of-a-sorted-array/)

```cpp
    vector<int> sortedSquares(vector<int>& nums) {
        vector<int>sq(nums.size());
        int l=0,r=nums.size()-1;
        for (int k=r;k>=0;k--)
        {
            if (abs(nums[l])>=abs(nums[r])) sq[k]=nums[l]*nums[l++];
            else sq[k]=nums[r]*nums[r--];
        }
        return sq;
    }
```
Time Complexity : O(n)\
Space Complexity : O(n)
  

4. [Duplicate Zeros](https://leetcode.com/problems/duplicate-zeros/)

```cpp

```
