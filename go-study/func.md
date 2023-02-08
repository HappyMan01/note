## 函数
golang中函数是一等公民

### 语法要点

1. 可以返回多个值(一般是结果和error错误)

2. 函数也可以作为参数
```go
func apply(op func(int, int) (int, error), a, b int) (int, error) {
	u := reflect.ValueOf(op).Pointer()
	s := runtime.FuncForPC(u).Name()
	fmt.Printf("func name is %s with args (%d %d)\n", s, a, b)
	return op(a, b)
}

func div(a, b int) (int, error) {
	if b == 0 {
		return -1, fmt.Errorf("by zero")
	} else {
		return a / b, nil
	}
}

// callled
apply(div ,4, 2)
```

3. go语言中没有什么默认参数啊，可选参数啊，方法重载啊，这些是都是没有的
只有一个可变参数
```go
func sum(numbers ...int) int {
	s := 0
	for _, n := range numbers {
		s += n
	}
	return s
}
func main() {
	fmt.Println(sum(1, 2, 3, 4))

}
```
