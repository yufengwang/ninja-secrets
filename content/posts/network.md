+++
author = ["wenhu"]
draft = false
+++

## 计算机网络相关面试题 {#计算机网络相关面试题}


### 三次握手 {#三次握手}

1.  client 发送 syn（Synchronize Sequence Number)到 server，表示想要建立 tcp 连接
2.  Server 发送(syn+ ack)
3.  client 发送 ack 给 server，连接建立


### 四次挥手 {#四次挥手}

1.  client 发送 FIN
2.  server 接收到 FIN，发送 ack
3.  server 发送 FIN
4.  client 发送 ack


### 网络分层 {#网络分层}


#### tcp/ip 模型 {#tcp-ip-模型}

1.  应用层
2.  传输层
3.  网络层
4.  链路层


#### OSI 模型 {#osi-模型}

1.  应用层
2.  展示层
3.  会话层
4.  传输层
5.  网络层
6.  链接层
7.  物理层