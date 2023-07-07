---
title: "测试脚本"
description: 
date: 2023-07-07T10:05:33Z
image: 
math: 
license: 
hidden: false
comments: true
draft: false
---

由于国内网络环境，以及 ARM 架构的问题，常见的 YABS 脚本并不适合所有设备。因此这里汇总一下用到的一些脚本。


### ARM 质数测试

```
apt-get update
apt install sysbench 
sysbench --num-threads=4 --test=cpu --cpu-max-prime=20000 run
```

### Geekbench 5 手动


```
wget http://cdn.geekbench.com/Geekbench-5.4.5-Linux.tar.gz
tar -zxvf Geekbench-5.4.5-Linux.tar.gz
cd Geekbench-5.4.5-Linux
./geekbench_x86_64
```

### YABS 国内


```bash
curl -sL https://gcore.jsdelivr.net/gh/masonr/yet-another-bench-script@master/yabs.sh | bash
# 跑 GB5
curl -sL https://gcore.jsdelivr.net/gh/masonr/yet-another-bench-script@master/yabs.sh | bash -s -- -5
```
### SpeedTest 国内

```bash
apt install speedtest-cli
speedtest-cli --list | grep China
speedtest-cli --server [SERVERID]
```




### REFERENCE

https://www.jianshu.com/p/7a0dc79ced11