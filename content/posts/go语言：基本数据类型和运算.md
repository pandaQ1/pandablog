+++
title = 'go语言：基本数据类型和运算'
date = 2026-09-08T00:43:27+08:00
tags = []
categories = ['go语言']
draft = false
+++

```go
package main

//包名 main
import (
	"fmt"
)

// 导入包 fmt: 打印函数
func main() {
	var a int = 10
	//变量整型声明并赋值
	var b float64 = 3.14
	//变量浮点型声明并赋值
	var c string = "Hello, World!"
	//变量字符串型声明并赋值
	var d bool = true
	//变量布尔型声明并赋值
	fmt.Println(a,b,c,d)
	//打印变量
	e,f:=10,3
	//多次声明并赋值，类型推断
	fmt.Println(e+f,e-f,e*f,e/f,e%f)
	//打印变量，加减乘除取模
}
```
