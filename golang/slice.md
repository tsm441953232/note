### slice底层结构
位于runtime/slice.go
```
type slice struct {
	array unsafe.Pointer  // 指针地址
	len   int // 长度
	cap   int // 容量
}
```
slice本身为引用类型，在使用make创建slice时会返回它本身，可以接受三个参数即类型，长度，容量  
初始化slice时，如果定义了大于0的长度，那么slice的值为该类型的默认值，int-0 bool-false  

### 扩容
我们在对slice进行append操作时会使slice扩容  
切片的扩容，就是当切片添加元素时，切片容量不够了，就会扩容  
扩容的大小遵循下面的原则：
+ 如果切片的容量小于1024个元素，那么扩容的时候slice的cap就翻倍
+ 一旦元素个数超过1024个元素，增长因子就变成1.25，即每次增加原来容量的四分之一
+ 如果扩容之后，未超过原切片的容量，那么切片中的指针指向的位置，就还是切片（这就是产生bug的原因）
+ 如果扩容之后，超过了原切片的容量，那么，Go就会开辟一块新的内存，把原来的值拷贝过来，这种情况丝毫不会影响到原切片（详见/testcode/slice_test.go）

### 数组和切片
+ 数组为定长，切片为变长
+ 在进行函数传递时，数组为值传递而切片为引用传递(切片本身就是引用类型)

### 线程安全
切片不是线程安全的，在对切片进行多协程操作时应进行lock  

线程A，list=append(list,1) ，这时候 list={1}，那么新的list就是list={1,1}
线程B，list=append(list,1) ，这时候 list={1}，那么新的list就是list={1,1}
而不是{1,1,1}，因为AB拿到的list是相同的地址，会导致A或者B被对方所覆盖
