## 1-1 application communication
双向的，可靠的字节流
1. World Wide Web(HTTP)
   client---server
   request: GET http://
   response:http:// 200 ok
2. BitTorrent: 一个程序，允许人们共享和交换大文件 
   与web不同，BitTorrent向其他客户端请求文档，是一个peer-to-peer模型
   为了使单个客户端可以并行地从许多其他客户端发出请求，BitTorrent将文件分成称为pieces的数据块。
   当客户端想要下载文件时，首先要找到一个叫做torrent的文件，它描述了要下载的数据文件的一些信息，还会告诉BitTorrent该torrent的tracker是谁。tracker是一个节点，用于跟踪哪些客户端是该swarm的成员。要join a torrent，你的客户端再次与tracker联系，以请求其他客户端的列表。你的客户端打开与其中一些客户端的连接，并开始请求pieces of file。这些客户端可以反过来请求pieces。
   当新客户端加入群时，tracker可能会告诉这个新客户端去连接你的客户端。
3. Skype
   与web不同，Skype有两个客户端，即两台互相请求数据的个人计算机。
   NAT(Network Address Translator)
   使用rendezvous server实现
   客户端A和B都位于NAT之后，则通过relay进行通信。

## 1-2 4层Internet模型
