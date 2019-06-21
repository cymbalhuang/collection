```
    1  wget https://git.io/vpnsetup-centos -O vpnsetup.sh
    2  yum install -y git
    3  yum install -y wget
    4  wget https://git.io/vpnsetup-centos -O vpnsetup.sh
    5  ll
    6  vi vpnsetup.sh 
    
    YOUR_IPSEC_PSK='cymbal'
    YOUR_USERNAME='xxx'
    YOUR_PASSWORD='xxx'
    
    7  sh vpnsetup.sh 
    8  yum install -y python-setuptools
    9  easy_install pip
   10  pip install git+https://github.com/shadowsocks/shadowsocks.git@master
   11  mkdir /etc/shadowsocks
   12  vi /etc/shadowsocks/config.json
   
   {
        "server": "0.0.0.0",
        "server_port": xxxx,
        "local_address": "127.0.0.1",
        "local_port": 1080,
        "password": "xxx",
        "timeout": 300,
        "method": "aes-256-cfb",
        "fast_open": false,
        "workers": 1
    }
   
   13  ssserver -c /etc/shadowsocks/config.json -d start
   
```
防火墙端口：

l2tp

udp:500
udp:4500
udp:1701

shadowsocks

tcp:8388

