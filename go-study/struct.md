## go 面型对象
1. 只支持封装不支持继承和多态
2. 没有class只有结构体
```go
// 定义一个学生class
type student struct {
	name string
	age  int
}

//  工厂函数可以当作构造器使用
func createStudent(name string, age int) *student {
	return &student{"gaoxingnan", 18}
}

main {
	// 定义一个student 
	var s student
	s1 := createStudent("hello", 11)
}
```
3. 定义结构体方法
```go
 
 // 定义一个学生类的打印方法
func (s student) print1() {
	fmt.Println(s)

}

// 定义一个setName 方法
// 需要传递一个指针类型(因为go语言中的所有都是值传递)
func (s *student) setName(name string) {
	s.name = name
}

	var s student
	s.name = "hello"
	s.age = 12
				s.print1() // {gaoxingnan 1}
	
```
