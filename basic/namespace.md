## 命名空间

### 概述

在`C++`中命名空间`namespace`是为了避免命名重复而出现的产物

### 声明

下面的代码声明了一个名字叫 `A` 的命名空间：

```cpp
namespace A 
{
    int cnt;
    void f(int x) { cnt = x; }
}  // namespace A
```

声明之后，在这个命名空间外部，你可以通过`A::f(x)`来访问命名空间`A`内部的`f`函数。

命名空间的声明是可以嵌套的，因此下面这段代码也是允许的：

```cpp
namespace A 
{
	namespace B 
    {
        void f() { ... }
    }  // namespace B
    void f() 
    {
        B::f();  // 实际访问的是 A::B::f()，由于当前位于命名空间 A 内，所以可以省略前面的 A::
    }
}  // namespace A
void f()  // 这里定义的是全局命名空间的 f 函数，与 A::f 和 A::B::f         
          // 都不会产生冲突
{
    A::f();
    A::B::f();
}
```



------

[想维护此页面？点我！](https://github.com/FBIWZH/cppsource/blob/main/basic/namespace.md)