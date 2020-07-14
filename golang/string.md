### string底层结构
数据结构位于/runtime/string.go stringStruct
```
type stringStruct Struct {
    str unsafe.Pointer // 起始地址
    len int // 长度
}
```

### copy
string 底层结构为unsafe指针以及字节的长度  
byte -> string 或者 string -> byte 都会进行内存拷贝  

### 详见/testcode/string_test.go