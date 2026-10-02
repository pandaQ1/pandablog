+++
title = 'c语言入门：关键字'
date = 2026-07-15T08:37:54+08:00
tags = []
categories = ['C语言']
draft = false
+++

**正确的 C89 关键字列表（共 32 个）：**

```c
auto     break    case     char     const    continue
default  do       double   else     enum     extern
float    for      goto     if       int      long
register return   short    signed   sizeof   static
struct   switch   typedef  union    unsigned void
volatile while
```

---

#### 核心规则

**1. 不能用作标识符（变量名、函数名、结构体名等）**
关键字是编译器预留的专用词，具有固定语法含义。
错误示例：

```c
int int;        // 错误，int 是关键字
signed signed;  // 错误，signed 是关键字
```

**2. 关键字全部小写，大小写敏感**
C 语言区分大小写，因此 `Int`、`If`、`WHILE` 等都不是关键字，可以合法地用作标识符（但极其不推荐，会降低可读性）。

**3. 关键字功能分类**

| 类别 | 关键字 |
| --- | --- |
| **数据类型** | `char`, `short`, `int`, `long`, `float`, `double`, `void`, `signed`, `unsigned` |
| **流程控制** | `if`, `else`, `for`, `while`, `do`, `switch`, `case`, `default`, `break`, `continue`, `goto`, `return` |
| **存储类别** | `auto`, `static`, `extern`, `register` |
| **复合类型** | `struct`, `union`, `enum`, `typedef` |
| **限定符** | `const`, `volatile` |
| **运算符关键字** | `sizeof` |

**分类说明：**

- `typedef` 用于为已有类型创建别名，因此归入复合类型相关。
- `const` 和 `volatile` 是类型限定符，用于修饰变量，表示只读或易变。
- `sizeof` 是一个编译时运算符，用于计算类型或变量占用的字节数，是 C 语言中唯一以关键字形式存在的运算符。

---

### 补充：C89 与后续标准的差异

| 关键字 | 引入标准 | 作用 |
| --- | --- | --- |
| `inline` | C99 | 建议编译器将函数内联展开 |
| `restrict` | C99 | 指针限定符，提示指针是访问数据的唯一方式 |
| `_Bool` | C99 | 布尔类型（头文件 `<stdbool.h>` 中 `bool` 是其宏） |
| `_Complex` / `_Imaginary` | C99 | 复数类型（如 `float _Complex`） |

学习 C89 时，不必考虑上述 C99 新增的关键字；若您的编译环境支持 C99 或更高标准，可以逐步了解它们。

---

这份修正版严格遵循 C89 标准，概念清晰，适合作为初学笔记使用。如果有需要进一步解释的分类，我可以再展开说明。
