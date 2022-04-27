channel 不仅允许你将值从一个goruntine发送到另一个goruntine，还确保在接收的goroutine尝试使用该值之前，发送的goroutine已经发送了该值。

channel通过blocking（阻塞）——暂停当前goroutine中的所有进一步操作来实现这一点。发送操作阻塞发送goroutine，直到另一个goroutine在同一channel上执行了接收操作。反之亦然：接收操作阻塞接收goroutine，直到另一个goroutine在同一channel上执行了发送操作。这个行为允许goroutine同步它们的动作——协调它们的时间。

声明一个channel
```go
var myChannel chan float64
myChannel = make(chan float64)

或

myChannel := make(chan float64)
```

## 使用channel发送和接收值
```go
// 发送值
myChannel <- 3.14
// 接收值
<- myChannel
```