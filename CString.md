# CString 使用指南
---
## 目录
1. 简介
2. 操作符
    1. **CString::operator =**
    2. CString::operator LSCTSTR
    2. CString::operator <<, >>
    2. CString::operator +
    5. CString::operator +=
    6. CString比较操作符
    7. CString::operator []
3. 成员函数
    1. CString::Compare
    2. CString::CompareNoCase 
3. 
## 简介
---
## 操作符
---
## 成员函数
---
### CString::Compare
- 函数原型：`int Compare( LPCTSTR lpsz ) const;`
- 介绍：`CString::Compare`用于比较两个字符串，参数为与本字符串相比较的另一字符串指针，返回值为`int`，如果两个字符串完全一致，则返回0；如果字符串比 `lpsz`小，则返回-1；如果比`lpsz`大，则返回1。值得注意的是，*字符串的比较是从最高位开始的*，例如`"abcdef"`比`"b"`小。
- 样例：
    ```c++
    CString str1("123456");
    CString str2("123455");
    cout << str1.Compare(str2);
    //输出为1
    
	CString str3("123455");
	CString str4("123455");
	cout << str3.Compare(str4);
    //输出为0
    ```
### CString::CompareNoCase
- 函数原型：`int CompareNoCase( LPCTSTR lpsz ) const;`
- 介绍：`CString::CompareNoCase`的功能与`CString::Compare`类似，都是用于比较两个字符串的大小，不同的是：`CString::CompareNoCase`忽略字符串的大小写情况。
- 样例：
    ```c++
    CString str1("ABC");
    CString str2("abc");
    cout << str1.CompareNoCase(str2);
    //输出为0
    ```
