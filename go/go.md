Go语言原生支持Unicode，它可以处理全世界任何语言的文本。


每个 Go 程序都是由包构成的。
程序从 main 包开始运行

导入包
```go
import (fmt) 
```
打印输出
```go
fmt.Println('hello go')
```

类型在变量名之后： num int

多值返回：函数可以返回任意数量的返回值

在函数中，简洁赋值语句 `:=` 可在类型明确得地方代替 `var`声明。

Go的基本类型：
```go
bool

string

int  int8  int16  int32  int64
uint uint8 uint16 uint32 uint64 uintptr

byte // uint8 的别名

rune // int32 的别名
    // 表示一个 Unicode 码点

float32 float64

complex64 complex128
```
`int`, `uint` 和 `uintptr` 在 32 位系统上通常为 32 位宽，在 64 位系统上则为 64 位宽。



在 go 中，当我们有一个值时，通常会把它分配给一个变量，但我们不打算使用这个值时，我们可以使用Go的空白标识符 `_` 。

在 go 中声明的每一个变量都有一个作用域：代码中“可见”的部分。声明的变量可以再其作用域内的任何地方被访问，但如果你试图在该作用域之外访问它，就会收到一个错误。

变量的作用域由其声明所在的块和嵌套在该块中的任何块组成。

参数是函数的局部变量，其值是在调用函数时设置的。当函数运行时，每个参数都将被设置为对应参数中值的**副本**。

指针允许函数改变变量所保存的原始值，而不是副本。

### 结构体
一个结构体（struct）就是一组字段（field）
```go
struct {
	field1 string // 字段名称 字段类型
	field2 string
}
```

### 类型定义
类型定义允许你自己创建新的类型。你可以基于基础类型来创建新的定义类型。
```go
type myType struct {
	// fields here
}
```
### 切片

每个数组的大小都是固定的。而切片则为数组元素提供动态大小的、灵活的视角。在实践中，切片比数组更常用。

类型 `[]T` 表示一个元素类型为 `T` 的切片。

切片通过两个下标来界定，即一个上界和一个下界，二者以冒号分隔：

a[low : high]

它会选择一个半开区间，包括第一个元素，但排除最后一个元素。

以下表达式创建了一个切片，它包含 `a` 中下标从 1 到 3 的元素：

a[1:4]