# C++ string 相關操作 

## 概要

> ### 初始化：

```cpp
#include <string>
using namespace std;

string str1 = "Hello";  
string str2("Hello");  
```

> ### 添加元素：

```cpp
str1.insert(5, " world");
```

> ### 刪除元素：

```cpp
str1.erase(5, 6); 
```

> ### 訪問元素：

```cpp
str1[0];
```

> ### 其他操作：

```cpp
str.length();  

string str3 = str1 + str2; 

if (str1 == str2){
	
}

str1.substr(3, 2); 

to_string(num); 
stoi(str); 


size_t pos = str1.find("lo");
if (pos != string::npos) {
    
} else {
   
}
```
  
## 詳細

> ### 初始化：

```cpp
#include <string>
using namespace std;

string str1 = "Hello";  
string str2("Hello");  //使用建構函數
```

> ### 添加元素：

```cpp
str1.insert(5, " world");  //在第5個位置插入字串world
```

> ### 刪除元素：

```cpp
str1.erase(5, 6); //從第5個位置開始刪除長度為6的字串
```

> ### 訪問元素：

```cpp
str1[0]; //訪問str1第0個位置的元素
```

> ### 其他操作：

```cpp
str.length();  //獲取字串長度

string str3 = str1 + str2; //str3為串接str1和str2的字串

if (str1 == str2){
	//字串符比較
}

str1.substr(3, 2); //在str1第3個位置開始取出長度為2的字串

to_string(num); //整數轉為字串
stoi(str); //字串轉為整數

//搜尋字串，找到的話會回傳位置，沒找到的話會回傳string::npos
size_t pos = str1.find("lo");
if (pos != string::npos) {
    // 找到子串
} else {
    // 未找到子串
}
```
