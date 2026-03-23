---
title: 2. NULL与nullptr
date: 2026-03-23 11:11:58
tags:
---


每当我们创建一个新指针变量后, 立刻进行初始化是一种避免野指针的好习惯.下面两种初始化方式都可以.

```
int* p1 = NULL;
int* p2 = 0;
```

C当中, ```#define NULL (void*)0```.    C++当中, ```#define NULL 0```

对于C++, 这会导致一个问题: 如果有一个重载函数, 通过**参数类型为整数或指针**进行重载, 那么当参数传入初始化为NULL的指针时, 函数会认为该参数应该执行整数重载函数. 考虑到```#define NULL 0```, 这是很容易理解的.
```
#include <iostream>

#重载 nullprint 函数
void nullprint(int num)
{
	printf("num: %d\n", num);
}
void nullprint(int* ptr)
{
	printf("ptr: %p\n", ptr);
}

int main()
{
	int* ptr = NULL;
	int num = 10;
	printf("2.nullptr\n");
	nullprint(num);
	nullprint(ptr);
	return 0;
}
```



为了解决这个问题, C++定义了**nullptr**. 
nullptr 专用于初始化空类型指针，不同类型的指针变量都可以使用 nullptr 来初始化, nullptr会根据变量类型隐式转换为相同的类型.
```
int*    ptr1 = nullptr;
char*   ptr2 = nullptr;
double* ptr3 = nullptr;
```

