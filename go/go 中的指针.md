`&` : Go 中 “地址“操作符， 获取变量的地址。

我们可以获取任何类型变量的地址。每一个变量的地址都是不同的。

而表示变量地址的值称为指针，因为它指向可以找到变量的位置。

## 指针类型
指针的类型可以写为一个 * 符号，后面跟着指针指向的变量的类型。
例如：指向一个 int 变量的指针的类型将被写为 * int

## 函数指针
可以从函数返回指针，只需要声明函数的返回类型是指针类型
```go
func createPointer() *float64 /* 声明函数返回一个float64 指针 */ {
	var myFloat = 98.4
	return &myFloat // 返回指定类型的指针
}

func main() {
	var myFloatPointer *float84 = createPointer() // 将返回的指针赋给一个变量
	fmt.Println(*myFloatPointer) // 打印指针处的值
}


```