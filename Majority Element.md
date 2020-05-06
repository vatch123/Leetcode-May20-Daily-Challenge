### Majority Element

Given an array of size n, find the majority element. The majority element is the element that appears more than ⌊ n/2 ⌋ times.

You may assume that the array is non-empty and the majority element always exist in the array.

Example 1:
``
Input: [3,2,3]
Output: 3
```
Example 2:
```
Input: [2,2,1,1,1,2,2]
Output: 2
```

```cpp
class Solution {
public:
    int majorityElement(vector<int>& nums) {
        unordered_map <int, int> freq;
        long n = nums.size();
        cout<<n;
        for(auto it=nums.begin(); it!=nums.end(); it++){
            freq[*it]++;
            if(freq[*it]>n/2)
                return *it;
        }
        return 0;
    }
};
```
