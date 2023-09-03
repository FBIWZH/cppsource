### 头文件

是C++重要的引入类和函数的方式，其重要性相当于`python`的`import`，`java`和`c#`的`using`，没有它你几乎无法使用`C++`。

如何使用？分以下两种情况：

- 如果是`C++`标准库可以通过这样的格式引入：

  ```cpp
  #include </*要引用的库名 例如：*/ iostream>
  ```

- 如果是自己写的外部库可以通过这样的格式引入：

  ```cpp
  #include "/*文件相对路径，例如：*/ myHeader.h"
  ```

  $tips:$一般来说自己写的库使用`.h`的后缀。

`C++`标准头文件的列表可以参考[C++ 标准库参考 | Microsoft Learn](https://learn.microsoft.com/zh-cn/cpp/standard-library/cpp-standard-library-reference?view=msvc-170),

在这里只介绍一个头文件`<bits/stdc++.h>`，这个标头囊括了所有C++的STL标准库的表头，但是它只能在`Mingw`中使用，如果你用的`VS`，则不能使用。

其实除了`C++`语言本身的STL以外在Mingw的`Gnu`标准中还有一些库和标准算法，这些都可以在算法竞赛中使用，具体介绍可以参见博客：[pbds食用教程 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/554840097)

------

[想维护此页面？点我！](https://github.com/FBIWZH/cppsource/blob/main/basic/include.md)

