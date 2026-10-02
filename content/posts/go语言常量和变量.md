+++
title = 'go语言:常量和变量'
date = 2026-09-08T00:33:33+08:00
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
	//主函数
	var name string = "李四"
	//声明整型变量并赋值
	var age = 20.23
	//声明变量并赋值，类型推断，变量类型取决于值
	name2 := "张三"
	//声明变量并赋值，类型推断，变量类型取决于值
	fmt.Println(name, age, name2)
	//打印变量
	var (
		//定义多个变量，用括号括起来，并赋值
		name3 string = "李四"
		//声明字符串变量并赋值
		age2  int    = 20
		//声明整型变量并赋值
		name4 string = "张三"
		//声明字符串变量并赋值

	)
	fmt.Println(name3, age2, name4)
	//打印变量
	const PI = 3.14
	//声明常量，用const关键字声明，常量值不能被修改
	const (
		//声明常量，用const关键字声明，常量值不能被修改
		PI2 = 3.14
		//声明常量
		PI3 = 3.14
		//声明常量
		PI4 = 3.14
		//声明常量
		PI5 = 3.14
		//声明常量
		//声明常量
		PI7 = 3.14
		//声明常量
		PI8 = 3.14
	)
}
```
