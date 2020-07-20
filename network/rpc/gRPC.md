### gRPC
RPC(Remote Procedure Call)即远程过程调用，允许一台计算机调用另一台计算机上的程序得到结果，而代码中不需要做额外的编程，就像在本地调用一样。
在rpc框架中主要有client、server、registry
rpc基本流程：
1. client以本地调用方式发起调用
2. client stub接收到请求后将方法参数等组装成网络传输的消息体
3. client stub找到服务地址，并将消息发送到服务端
4. server stub收到消息后进行解码
5. server stub根据解码结果调用本地的服务
6. server执行并将结果返回给server stub
7. server stub将返回结果打包成消息并发送至调用方
8. client stub接收到消息，并进行解码
9. 调用方得到最终结果

