目的主机监听(**注意不要颠倒，不然原文件被删除！！！**)

nc -l 监听端口[ 未使用端口] > 要接收的文件名 

nc -l 5555 > cache.tar.gz 

源主机发起请求 

nc 目的主机ip 目的端口 < 要发送的文件 

nc 192.168.0.85 5555 < /root/cache.tar.gz 

如出现Ncat: No route to host，可能是防火墙不通，如虚拟机，可用iptables -F命令清除防火墙
