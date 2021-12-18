leetcode 

### twosum | EASY


### Success

12/18/2021 15:26	Accepted	12 ms	10.9 MB	cpp

### Details 
Runtime: 
12 ms, faster than 77.76% of C++ online submissions for Two Sum.

Memory Usage: 
10.9 MB, less than 29.62% of C++ online submissions for Two Sum.



### code
```
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int, int> table;

        for(int i = 0; i < nums.size(); i++) {
            // If not in the table, insert the index
            if( table.find( target - nums[i] ) == table.end() ) {
                table[ nums[i] ] = i;
            }
            else {
                return { table[ target-nums[i] ], i };
            }
        }

        return {};
    }
};
```
