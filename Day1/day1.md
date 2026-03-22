# Day1
## 基础知识：
1. 函数中传入数组要加&；vector<int>& nums;
2. 构造vector方式：｛map[complement],i｝ {a,b};vector<int> v{1,2,3}
3. 访问方式：v[i];末尾加元素：v.push_pack(x); 清空：v.clear(); 判空：v.empty()
4. vector有.size()用法；map有.find(key),.end()（迭代器（类似于指针）指向最后一个函数的下一个位置）的函数，常用此方法遍历。
5. ++i与i++
int i = 0;
out << i++ << endl; // 输出 0（先输出原值，再+1），i 最终变为 1
cout << ++i << endl; // 输出 2（先+1，再输出新值），i 最终变为 2

## 算法实现：
1. unordered_map map.find():遍历复杂度为O（1）；需要注意的是map的.find()函数遍历不是O（1）；
原因：unordered_map底层是哈希表，key算作一个hash值；map为红黑树，.find()遍历为O（N）；
