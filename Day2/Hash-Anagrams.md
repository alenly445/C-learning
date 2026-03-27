
```
#include <iostream>
#include <unordered_map>
#include <algorithm>
#include <string>
#include <vector>
using namespace std;
class Solution{
public:
    vector<vector<string>> groupAnagrams(vector<string>& strs){
        unordered_map<string,vector<string>> anagramMap;
        for(string& str: strs){
            string key=str;
            sort(key.begin(),key.end());
            anagramMap[key].push_back(str);
        }
        vector<vector<string>> final;
        for(const auto& entry:anagramMap){
            final.push_back(entry.second);
        }
        return final;
    }
};
```
# 基础知识
1. sort() 函数：来自头文件<algotithm>，key.begin()是第一个字符的迭代器，key.end()是最后一个字符下一个位置的迭代器，sort()会按照ASCII码顺序把区间[begin,end)内的字符串排序。
2. for(const auto& entry:  )，for(string&str: strs)用法见Day1。

# 算法实现
