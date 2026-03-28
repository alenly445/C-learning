```
#include <vector>
#include <unordered_set>
#include <algorithm>
using namespace std;

class Solution {
public:
    int longestConsecutive(vector<int>& nums) {
        unordered_set<int> num_set(nums.begin(), nums.end());
        int max_len = 0;
        
        for (int num : num_set) {
            // 只有当前数是连续序列的起点时才开始计算
            if (!num_set.count(num - 1)) {
                int current_num = num;
                int current_len = 1;
                
                // 向后查找连续的数
                while (num_set.count(current_num + 1)) {
                    current_num++;
                    current_len++;
                }
                
                max_len = max(max_len, current_len);
            }
        }
        return max_len;
    }
};

```
