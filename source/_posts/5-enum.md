---
title: 5-enum
date: 2026-05-16 10:29:07
tags:
categories:
---
只介绍enum class

---

## 问题与需求

enum class的本质作用是 **给具有标识意义的int变量加作用域，使bug在编译期能够被发现**

具有标识意义，一般指状态码

比如下面的例子：
```C++
// 不用enum
int OK=0,

ERROR=1,

UNKNOWN=-1;

void status_check(int status) {

if (status == 0) {

printf("OK\n");

} else if (status == 1) {

printf("ERROR\n");

} else if (status == -1) {

printf("UNKNOWN\n");

}

}
```

这样写可能会导致2个问题：
1.  0,1,-1这种数字的意义并不明确，可能过几天自己就忘了哪个数对应哪个状态。
2. 假如代码写错了，把别的int变量错当成```
   status```传到```
   status_check```函数里，编译时不会报错，运行时出问题

所以需要给status做一些设置，使状态码可读性增强，并且把status和普通int变量区分开

这就是enum class要做的事

---

## 具体语法

声明语法：
```C++
enum class 枚举名 [: 底层类型] { 枚举值1 [= 初始值], 枚举值2, ... };
```

比如：
```C++
enum class Status : uint8_t { OK = 0, Error = 1, Timeout = 2 };
```

```[]``` 代表可选，这部分加不加都行。底层类型默认int，**初始值默认从0开始递增1**

也就是说，下面的写法也是对的：
```C++
enum class Status :  { OK, Error, Timeout };
```

和上面的写法区别就是类型为int




