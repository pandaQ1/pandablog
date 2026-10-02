+++
title = 'go语言：数组的基本使用'
date = 2026-09-08T01:23:47+08:00
tags = []
categories = ['go语言']
draft = false
+++

```go
package main

//包名 main
import "fmt"

// 导入包 fmt: 打印函数
func main() {
	scores := [3]int{1, 2, 3}
	//声明整型数组并赋值，索引从0开始
	scores[1] = 100
	//将scores数组下标为1的数改为100
	fmt.Println(scores)
	//打印数组
	fmt.Println(scores[0])
	fmt.Println(scores[2])
	fmt.Println(scores[1])
	//打印指定下标的数组
	fmt.Println(len(scores))
	//打印数组长度
	var arr [3]int
	//声明整型数组未赋值，默认值为0
	fmt.Println(arr)
	//打印展示未赋值默认值为0
	arr[0] = 10
	arr[1] = 20
	arr[2] = 30
	//将为赋值的数组元素赋值
	fmt.Print(arr)
	//打印已赋值的数组
	arr2 := [...]int{1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
	//声明一个数组，未定义长度，则长度根据数组元素决定长度
	fmt.Println(arr2)
	//打印未定义长度的数组元素
	fmt.Println(len(arr2))
	//打印未定义长度的数组长度
	for i := 0; i < len(arr2); i++ {
		fmt.Println(arr2[i])
	} //for循环遍历数组
}
```
