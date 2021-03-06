指针是可见的内存地址，`&`操作符可以返回一个变量的内存地址，并且`*`操作符可以获取指针指向的变量内容，但是在Go语言里没有指针运算，也就是不能像c语言里可以对指针进行加或减操作。

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

## 指针
指针：Go 拥有指针。指针保存了值的内存地址。
类型 `*T` 是指向 `T` 类型值的指针。其零值为 `nil`。

```go
var p *int
```

`&` 操作符会生成一个指向其操作数的指针。

```go
i := 42
p = &i
```


`*` 操作符表示指针指向的底层值。

```go
fmt.Println(*p) // 通过指针 p 读取 i
*p = 21         // 通过指针 p 设置 i
```

这也就是通常所说的“间接引用”或“重定向”。