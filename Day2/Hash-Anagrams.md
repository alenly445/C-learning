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
