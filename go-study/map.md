### map
map在go语言中是对hash表(存储了一个key/value的无序集合)的引用，创建一个map就是创建了一个对hash表的引用，map这种数据结构，查询更新删除都能够达到常数复杂度

## 声明
1. make 声明
```go
  names := make(map[string]int)
 
 names["hello"] = 1
  names["world"] = 2
```
2. var 声明
```go
  var names = map[string]int{"hello", 1, "world": 2}
```
3. 简短声明
```go
  names := map[string]int{"hello", 1, "world": 2}
```

## 操作
1. 查询
```go
  // 查询是否存在某一个值
  value, ok := names["hello"] // value 表示k对应的值，ok表示是否存在`hello` 这个key

  // 遍历map得到key和所对应的value
  for key,value range names {
      fmt.Println(key,value)
    }
```
2. 添加
```go
  names["tom"] = 4 // 添加key为tom，value为4
```
3. 删除
```go
  // 使用内置函数delete
  delete(names, "hello") // 删除names中hello这个key
```
4. 修改
```go
  name["hello"] = 9 // 把中的hello对应的value赋值为9
```
5. 判断两个map是否相等
 * 判断长度不等就反悔false
 * 把其中一个map的key放在另一个map中去查询，返回的ok是false或者返回的值和另一个map的值不想等，也返回false
 * 最后返回true
 ```go
  func equal(x, y map[string]int) bool {
    if len(x) != len(y) {
        return false
    }
    for k, xv := range x {
        if yv, ok := y[k]; !ok || yv != xv {
            return false
        }
}
return true }
 ```
### set
 go语言中并没有实现set，我们可以同过map来实现set集合，因为map中的key不一样(这一点我觉得并没有什么问题)
