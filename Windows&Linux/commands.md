### 网络参数
```shell
ip地址: 
	ifconfig eth0 xxx.xxx.xxx.xxx netmask 255.255.255.0
默认网关:
	route add default gwxxx.xxx.xxx.xxx
DNS服务器:
    echo nameserver xxx.xxx.xxx.xxx > /etc/resolv.conf
```


### 在文件中修改
```shell
/etc/network/interfaces

auto eth0 
iface eth0 inet static
address xxx.xxx.xxx.xxx
netmask 255.255.255.0
network xxx.xxx.xxx.0
broadcast xxx.xxx.xxx.255
gateway xxx.xxx.xxx.254
```

### apt命令
    apt-get update 更新至最新
    apt-get upgrade 更新所有
    apt-get dist-upgrade 所有软件升至最新

### nmap命令
```shell
nmap xxx.xxx.xxx.xxx //扫描指定ip地址
nmap xxx.xxx.xxx.xxx-xxx  //扫描一定范围内端口
nmap -sn  //只检查是否在线
nmap -PN  //不对目标进行PING处理
nmap -PR  //使用arp协议检查
namp -sS  //使用TCP半开扫描
namp -sT  //全开扫描
namp -sU  //使用UDP协议扫描
nmap -p "*" xxx.xxx.xxx.xxx  //扫描改地址下所有端口
nmap -p 端口号 xxx.xxx.xxx.xxx  //扫描指定端口
nmap --top-ports n xxx.xxx.xxx.xxx //扫描使用频率最高的n个端口
nmap -O xxx.xxx.xxx.xxx  //目标操作系统
 nmap -sV xxx.xxx.xxx.xxx  //扫描目标服务
 nmap -oX  //对目标扫描结果保存为xml格式
```
