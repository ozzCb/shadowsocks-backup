## install ShadowSocks for ubuntu 16.04

### install the server
`wget --no-check-certificate -O shadowsocks-libev.sh https://raw.githubusercontent.com/uxh/shadowsocks_bash/master/shadowsocks-libev.sh && bash shadowsocks-libev.sh`

### install shadowsocks-qt5

```
sudo add-apt-repository ppa:hzwhuang/ss-qt5
sudo apt-get update
sudo apt-get install shadowsocks-qt5
```

### install proxychains
```
sudo apt install proxychains
# or compile proxychains4
git clone https://github.com/rofl0r/proxychains-ng.git
./configure --prefix=/usr --sysconfdir=/etc
make
sudo make install
sudo make install-config  #(installs proxychains.conf)
```

### config proxychains
```
sudo vim /etc/proxychains.conf
[ProxyList]
# add proxy here ...
# meanwile
# defaults set to "tor"
socks5 	127.0.0.1 1080
```

