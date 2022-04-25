```go
var myArray [5]int // 数组指定大小
var mySlice []int // 切片不指定大小
```

## 切片
调用内建的make函数，传递切片的类型和长度
```go
notes := make(string[], 7) 
```
切片字面量
```go
notes := []sting{"do", "re"}
```

### 使用“append”函数在切片上添加数据
Go提供一个内建的函数append来将一个或者多个值追加到切片的末尾。
所以我们调用append函数，惯例是将函数的返回值赋给你传入的那个切片变量。如果你只保存一个切片，你就无须考虑两个切片是否共享了同一个底层数组。