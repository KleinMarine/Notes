# C++ vector 相關操作 

## 概要

> ### 初始化：

```cpp
#include <vector>
using namespace std;

vector<int> vec; 
vector<int> vec(10); 
vector<int> vec(10, 1); 
vector<int> vec{0, 1, 2, 3, 4, 5}; 
```

> ### 添加元素：

```cpp
vec.push_back(6);
vec.insert(vec.begin(), 99);
```

> ### 刪除元素：

```cpp
vec.pop_back();
vec.erase(vec.begin());
vec.clear();
```

> ### 訪問元素：

```cpp
vec[0];
vec.at(0);
vec.front();
vec.back();
```

> ### 其他操作：

```cpp
vec.size();
vec.empty();
vec.resize(20);
vec.reserve(30);
accumulate(vec.begin(), vec.end(), 0);
```
  
## 詳細

> ### 初始化：

```cpp
#include <vector>
using namespace std;

vector<int> vec; // 初始化
vector<int> vec(10); // 指定大小為10
vector<int> vec(10, 1); // 指定大小為10且初始值為1
vector<int> vec{1, 2, 3, 4, 5}; // 初始化且初始值為1 2 3 4 5
```

> ### 添加元素：

```cpp
vec.push_back(6); // 在末端添加元素6
vec.insert(vec.begin(), 99); // 在 index = 0 的位置插入元素99
vec.insert(vec.begin() + 4 , 88); // 在 index = 4 插入元素88
```

> ### 刪除元素：

```cpp
vec.pop_back(); // 刪除末尾元素
vec.erase(vec.begin()); // 刪除 index = 0 的元素
vec.erase(vec.begin() + 4); // 刪除 index = 4 的元素
vec.clear(); // 清空所有元素
```

> ### 訪問元素：

```cpp
vec[0]; // 訪問 index = 0 的元素
vec.at(0); // 訪問 index = 0 的元素，如果超出範圍會拋出異常
vec.front(); //取出vec第一個元素
vec.back(); //取出vec最後一個元素
```

> ### 其他操作：

```cpp
vec.size(); //獲取元素個數
vec.empty(); //vector是否為空
vec.resize(5); // 改變大小為 5
vec.reserve(30); // 預留容量為 30
accumulate(vec.begin(), vec.end(), 0); //從vec.begin()開始累加vec的元素直到vec.end()，初始值為0
```


