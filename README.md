# DHT-Spider
A DHT Spider allows you to sniff the torrents and magnets.You can download what the script sniffed via magnets or torrents directly.

一个DHT爬虫，允许你嗅探种子和磁力链接。你可以通过磁力链接或种子文件直接下载资源。

![](/2017-07-24-204708_680x336_scrot.png)

# Usage
```./dht_spider.py [option]```  
```[-s]```: This option will not storage any file on your computer.Just print the informations on terminal.  
```[-s]```: 此选项将不会在您的计算机上存储任何文件。只会在终端上输出信息。

```[-p:filename]```: Where you want to storage magnets.  
```[-p:filename]```: 你想存储磁力链接的位置。

```[-h]```: Print this help and exit.  
```[-h]```: 输出此帮助并退出。

```[-t:thread num]```: How many thread to get the torrents metadata.  
```[-t:thread num]```: 解析种子元数据的线程数。

```[-b:(0|1)]```: 0-Do not save the torrent file. 1-Save the torrent file.  
```[-b:(0|1)]```: 0-不要存储种子文件。 1-存储种子文件。

When you get the magnet or torrent file.You should add the one of them into the Bittorrent Client.If few time later,there still haven't got  any node.You should add the sender's IP and port to be a peer(Normally,you can find sender's information in magnets file or terminal logs).Then,the file will begin to download.

当你获得了磁力链接或者种子文件。你必须添加两者之一到BT客户端中。如果几分钟后，仍然没有任何节点。你需要将发送者的IP和端口添加为对等连接（通常情况下，你可以在magnets文件或终端日志中找到发送者的信息）。然后，文件就会开始下载。

# Tips
1. If you use the same ```filename``` when you run the script again,the script will not storage or display the storaged magnet and torrent.  
如果你在第二次运行脚本时使用了相同的```filename```，脚本将不会再次显示或存储已存储的磁力链接和种子文件。

2. The script will check the info's infohash and announce's token automatically.  
脚本会自动验证info字段的infohash以及announce的令牌。

3. The default option is ```./dht_spider -p:hash.log -t:100 -b:1```.  
默认的选项是```./dht_spider -p:hash.log -t:100 -b:1```。

# Principle
[DHT Network theory and how to make a DHT Spider](https://lexuge.github.io/jekyll/update/2017/07/22/DHT%E7%BD%91%E7%BB%9C%E8%AF%A6%E8%A7%A3%E4%B8%8EDHT%E7%88%AC%E8%99%AB%E7%BC%96%E5%86%99%E6%8C%87%E5%8D%97.html)  
[DHT网络详解与DHT爬虫编写指南](https://lexuge.github.io/jekyll/update/2017/07/22/DHT%E7%BD%91%E7%BB%9C%E8%AF%A6%E8%A7%A3%E4%B8%8EDHT%E7%88%AC%E8%99%AB%E7%BC%96%E5%86%99%E6%8C%87%E5%8D%97.html)

# Thanks
This project are using following articles and projects:  
本项目的诞生离不开下面的文章/项目：

[Kademlia、DHT、KRPC、BitTorrent 协议、DHT Sniffer](http://www.cnblogs.com/LittleHann/p/6180296.html)（引用了BEP_0009协议的实现并对其进行错误的改正与改进）  
[simDHT](https://github.com/fanpei91/simDHT)（引用了get_peer,find_node,announce_peer的实现，并进行重新封装，实现多线程）

# License
This project is using AGPL-3.0+  
本项目使用AGPL 3.0或更新版本的协议。
