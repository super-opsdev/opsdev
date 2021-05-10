# opsdev
opsdev博客
==========
# vmware虚拟机部署
## 安装完成后，无法获取ip地址
我使用的是桥接模式，设置-->网络适配器，改成了桥接模式。
登录系统
、、、
vi /etc/sysconfig/network-scripts/ifcfg-ens33
、、、
修改 
、、、
BOOTPROTO=yes
ONBOOT=yes
、、、
然后重启网卡
、、、
systemctl restart network
、、、
