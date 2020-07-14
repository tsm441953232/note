### map底层结构
数据结构位于/runtime/map.go hmap  
map使用hashtable作为底层数据结构，解决hash冲突方式使用链地址法(链表)
```
type hmap struct {
    count       // 元素个数
    flags       // 元素标识
    B           // 最多负载  loadFactor*2<<B  loadFactor := count / (2^B)阈值为6.5
    noveflow    // 溢出的个数
    hash0       // hash种子

    buckets     // 数组长度(2<<B)个元素集合
    oldbuckets  // 扩容前的数组，2<<B-1，只有在扩容时有值
    nevacuate   // 扩容进度，小于这个地址都已经被迁移到新bucket
    extra       // optional fields
}
```

### TODO

#### map遍历是随机的
map在扩容的时候会进行rehash，顺序会发生改变，没有发生扩容的时候顺序是一定的
golang为了不让使用以来这种不可靠的顺序，在遍历的时候加入了随机数，所以在遍历的时候都是随机的

#### 线程安全
map不是线程安全的，并发读写会造成panic

TODO:
[map深度解析](https://www.cnblogs.com/qcrao-2018/p/10903807.html)