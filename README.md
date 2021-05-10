# opsdev
opsdev博客
==========
# vmware虚拟机部署
## 安装完成后，无法获取ip地址
我使用的是桥接模式，设置-->网络适配器，改成了桥接模式。
登录系统
```
vi /etc/sysconfig/network-scripts/ifcfg-ens33
```
修改 
```
BOOTPROTO=yes
ONBOOT=yes
```
然后重启网卡
```
systemctl restart network
```

# K8S部署教程
## 环境准备
1、关闭防火墙
```
systemctl stop firewalld
```
2、关闭selinux
```
sed -i 's/enforcing/disabled/' /etc/selinux/config
```
3、关闭swap分区
```
sed -ri 's/.*swap.*/#&/' /etc/fstab
```
4、设置主机名
```
hostnamectl set-hostname  k8s-master
```
 
