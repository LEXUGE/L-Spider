# DHT-Spider
A DHT Spider allows you to sniff the torrents and magnets.You can download what the script sniffed via magnets or torrents directly.

一个DHT爬虫，允许你嗅探种子和磁力链接。你可以通过磁力链接或种子文件直接下载资源。

![](/2017-07-22-103921_680x336_scrot.png)

# Usage:
```./dht_spider.py [-t|filename] [thread number]```

```-t```:This option will not storage any file on your computer.Just print the informations on terminal.

```-t```:此选项将不会在你的计算机上存储任何文件。只会在终端上输出信息。

```filename```:Where you want to storage magnets.

```filename```:存储magnets的文件路径。

```thread num```:How many thread to get the torrents metadata.

```thread num```:获取种子文件metadata的线程数。

When you get the magnet or torrent file.You should add the one of them into the Bittorrent Client.If few time later,there still haven't got  any node.You should add the sender's IP and port to be a peer(Normally,you can find sender's information in magnets file or terminal logs).Then,the file will begin to download.

当你获得了磁力链接或者种子文件。你必须添加两者之一到BT客户端中。如果几分钟后，仍然没有任何节点。你需要将发送者的IP和端口添加为对等连接（通常情况下，你可以在magnets文件或终端日志中找到发送者的信息）。然后，文件就会开始下载。
