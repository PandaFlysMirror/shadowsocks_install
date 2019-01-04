![Shadowsocks](https://github.com/miaocloud/shadowsocks_install/raw/master/shadowsocks.png)
# Auto install Shadowsocks Server

shadowsocks.sh
===============
- Auto Install Shadowsocks(Python) Server for CentOS/Debian/Ubuntu
使用方法：
使用root用户登录，运行以下命令：

wget --no-check-certificate -O shadowsocks.sh https://raw.githubusercontent.com/miaocloud/shadowsocks_install/master/shadowsocks.sh
chmod +x shadowsocks.sh
./shadowsocks.sh 2>&1 | tee shadowsocks.log
卸载方法：
使用root用户登录，运行以下命令：
./shadowsocks.sh uninstall
单用户配置文件示例（2015 年 08 月 28 日修正）：
配置文件路径：/etc/shadowsocks.json

{
    "server":"0.0.0.0",
    "server_port":your_server_port,
    "local_address":"127.0.0.1",
    "local_port":1080,
    "password":"your_password",
    "timeout":300,
    "method":"your_encryption_method",
    "fast_open": false
}
多用户多端口配置文件示例（2015 年 08 月 28 日修正）：
配置文件路径：/etc/shadowsocks.json

{
    "server":"0.0.0.0",
    "local_address":"127.0.0.1",
    "local_port":1080,
    "port_password":{
         "8989":"password0",
         "9001":"password1",
         "9002":"password2",
         "9003":"password3",
         "9004":"password4"
    },
    "timeout":300,
    "method":"your_encryption_method",
    "fast_open": false
}
使用命令（2015 年 08 月 28 日修正）：
启动：/etc/init.d/shadowsocks start
停止：/etc/init.d/shadowsocks stop
重启：/etc/init.d/shadowsocks restart
状态：/etc/init.d/shadowsocks status
=============================================
shadowsocks-libev.sh
===============
- Auto Install Shadowsocks(libev) Server for CentOS
- 使用方法：
使用root用户登录，运行以下命令：
wget --no-check-certificate -O shadowsocks-libev.sh https://raw.githubusercontent.com/miaocloud/shadowsocks_install/master/shadowsocks-libev.sh
chmod +x shadowsocks-libev.sh
./shadowsocks-libev.sh 2>&1 | tee shadowsocks-libev.log
卸载方法：
使用 root 用户登录，运行以下命令：
./shadowsocks-libev.sh uninstall
使用命令：
启动：/etc/init.d/shadowsocks start
停止：/etc/init.d/shadowsocks stop
重启：/etc/init.d/shadowsocks restart
查看状态：/etc/init.d/shadowsocks status
===================================================================
shadowsocks-libev-debian.sh
===============
- Auto Install Shadowsocks(libev) Server for Debian/Ubuntu
- 使用方法：
使用根用户登录，运行以下命令：
wget --no-check-certificate -O shadowsocks-libev-debian.sh https://raw.githubusercontent.com/miaocloud/shadowsocks_install/master/shadowsocks-libev-debian.sh
chmod + x shadowsocks-libev-debian.sh
./shadowsocks-libev-debian.sh 2>＆1 | tee shadowsocks-libev-debian.log
卸载方法：
使用root用户登录，运行以下命令：

./shadowsocks-libev-debian.sh卸载
使用命令：
启动：/etc/init.d/shadowsocks start 
停止：/etc/init.d/shadowsocks stop 
重启：/etc/init.d/shadowsocks restart 
查看状态：/etc/init.d/shadowsocks status
=======================================================================================================================================
shadowsocks-go.sh
===============
- Auto Install Shadowsocks(Go) Server for CentOS/Debian/Ubuntu
- 使用方法：
使用root用户登录，运行以下命令：
wget --no-check-certificate -O shadowsocks-go.sh https://raw.githubusercontent.com/miaocloud/shadowsocks_install/master/shadowsocks-go.sh
chmod +x shadowsocks-go.sh
./shadowsocks-go.sh 2>&1 | tee shadowsocks-go.log
卸载方法：
使用 root 用户登录，运行以下命令：
./shadowsocks-go.sh uninstall
安装完成后即已后台启动 Shadowsocks-go ，运行：
/etc/init.d/shadowsocks status
可以查看 Shadowsocks-go 进程是否已经启动。
本脚本安装完成后，已将 shadowsocks-go 加入开机自启动。
使用命令：
启动：/etc/init.d/shadowsocks start
停止：/etc/init.d/shadowsocks stop
重启：/etc/init.d/shadowsocks restart
状态：/etc/init.d/shadowsocks status
==========================================================================================
shadowsocksR.sh
===============
- Auto Install ShadowsocksR Server for CentOS/Debian/Ubuntu
- 使用方法：
使用root用户登录，运行以下命令：

wget --no-check-certificate https://raw.githubusercontent.com/miaocloud/shadowsocks_install/master/shadowsocksR.sh
chmod +x shadowsocksR.sh
./shadowsocksR.sh 2>&1 | tee shadowsocksR.log
卸载方法：
使用 root 用户登录，运行以下命令：

./shadowsocksR.sh uninstall
安装完成后即已后台启动 ShadowsocksR ，运行：

/etc/init.d/shadowsocks status
可以查看 ShadowsocksR 进程是否已经启动。
本脚本安装完成后，已将 ShadowsocksR 自动加入开机自启动。

使用命令：
启动：/etc/init.d/shadowsocks start
停止：/etc/init.d/shadowsocks stop
重启：/etc/init.d/shadowsocks restart
状态：/etc/init.d/shadowsocks status

配置文件路径：/etc/shadowsocks.json
日志文件路径：/var/log/shadowsocks.log
代码安装目录：/usr/local/shadowsocks

多用户配置示例：

{
"server":"0.0.0.0",
"server_ipv6": "[::]",
"local_address":"127.0.0.1",
"local_port":1080,
"port_password":{
    "8989":"password1",
    "8990":"password2",
    "8991":"password3"
},
"timeout":300,
"method":"aes-256-cfb",
"protocol": "origin",
"protocol_param": "",
"obfs": "plain",
"obfs_param": "",
"redirect": "",
"dns_ipv6": false,
"fast_open": false,
"workers": 1
}
=================================================================
shadowsocks-all.sh
==================
- Auto Install Shadowsocks Server (all version) for CentOS/Debian/Ubuntu
- 使用root用户登录，运行以下命令：

wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/miaocloud/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
启动脚本
启动脚本后面的参数含义，从左至右依次为：启动，停止，重启，查看状态。

Shadowsocks-Python 版：
/etc/init.d/shadowsocks-python start | stop | restart | status

ShadowsocksR 版：
/etc/init.d/shadowsocks-r start | stop | restart | status

Shadowsocks-Go 版：
/etc/init.d/shadowsocks-go start | stop | restart | status

Shadowsocks-libev 版：
/etc/init.d/shadowsocks-libev start | stop | restart | status

各版本默认配置文件
Shadowsocks-Python 版：
/etc/shadowsocks-python/config.json

ShadowsocksR 版：
/etc/shadowsocks-r/config.json

Shadowsocks-Go 版：
/etc/shadowsocks-go/config.json

Shadowsocks-libev 版：
/etc/shadowsocks-libev/config.json
=============================================================
haproxy.sh
===============
- Auto Install haproxy for Shadowsocks Server
- 使用方法：
使用root用户登录，运行以下命令：

wget --no-check-certificate https://raw.githubusercontent.com/miaocloud/shadowsocks_install/master/haproxy.sh
chmod +x haproxy.sh
./haproxy.sh
第一步输入需要 haproxy 代理的端口号，这里要跟 Shadowsocks 服务器开放的端口号一致。
第二步输入 Shadowsocks 公网 IPv4（注意：不是 haproxy 本机的 IP 地址）

安装完成后，脚本提示如下：

Congratulations, haproxy install completed.
Your haproxy Server IP: your_haproxy_server_ip
Your haproxy Server port: your_haproxy_server_port
Your Input Shadowsocks IP: your_shadowsocks_server_ip

Welcome to visit:https://shadowsocks.be/10.html
Enjoy it.

卸载方法：
使用 root 用户登录，Debian 或 Ubuntu 系统运行以下命令：

apt-get -y remove haproxy
CentOS 系统运行如下命令：

yum -y remove haproxy
然后再删除 haproxy 的配置文件目录即可，命令如下：

rm -rf /etc/haproxy
使用命令：
启动：service haproxy start
停止：service haproxy stop
重启：service haproxy restart
状态：service haproxy status

配置文件路径：/etc/haproxy/haproxy.cfg

其他说明：

1、在安装此脚本之前，请确保 Shadowsocks 服务器能正常使用，也就是说，你直接连上 Shadowsocks 服务器的可用的。
如何一键搭建 Shadowsocks 服务器，请参考本站相关文章。

2、如果你需要代理多个端口，请自行修改 haproxy 的配置文件 /etc/haproxy/haproxy.cfg
修改如下所示的部分：

frontend ss-8989
bind *:8989
default_backend ss-8989
backend ss-8989
server server1 111.222.111.222:8989 maxconn 20480

111.222.111.222 是示例 IP，你需要改成你自己的 Shadowsocks 服务器 IP 地址。
其中，frontend 和 backend 是成对出现的。如果你需要添加更多端口，只需复制这两处，并做相应修改即可。
frontend 是 haproxy 使用的端口，backend 是连接 Shadowsocks 服务器的端口。我这里为避免混淆，把两者端口统一了。

3、客户端配置说明
client

服务器IP：此处填写 haproxy 服务器的公网 IP（脚本最后显示的 Your haproxy Server IP）
服务器端口：此处填写 haproxy 服务器代理的端口（脚本最后显示的 Your haproxy Server port）
密码：此处填写 Shadowsocks 服务器所对应的端口的密码
加密：此处选择 Shadowsocks 服务器所对应的端口的加密方式
协议：此处可选，如果你安装的是 ShadowsocksR 服务端可选择，默认即可
混淆：此处可选，如果你安装的是 ShadowsocksR 服务端可选择，默认即可

4、本脚本没有对防火墙进行任何设置。因此，在安装完毕后，如果你发现连接不上，可以尝试更改防火墙设置或关闭防火墙。

5、值得注意的是，haproxy 只能使用 TCP 方式中转流量。
Copyright (C) 2014-2018 Teddysun
