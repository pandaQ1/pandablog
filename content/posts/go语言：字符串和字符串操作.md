+++
title = 'go语言：字符串和字符串操作'
date = 2026-09-08T00:57:23+08:00
tags = []
categories = ['go语言']
draft = false
+++

```go
package main

//包名 main
import "fmt"
// 导入包 fmt: 打印函数
import "strings"
//导入包 strings：字符串函数
func main() {
	c:="Hello, World!"
	//声明变量并赋值，类型推断
	fmt.Println(c)
	//打印变量
	fmt.Println(len(c))
	//打印变量长度
	fmt.Println(strings.ToUpper(c))
	//打印变量大写
	fmt.Println(strings.Contains(c,"Hello"))
	//打印变量是否包含Hello
	fmt.Println(strings.Split(c,","))
	//打印变量分割
	fmt.Println(strings.Replace(c,"Hello","你好",1))
	//打印变量替换
}
```
