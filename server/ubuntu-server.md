前言
-----

Ubuntu Server操作经验

1993年具有Linux血统的Debian操作系统诞生了，2004年10月Debian的衍生操作系统Ubuntu诞生。

Ubuntu坚持每半年发布一个版本至今，其版本号命名方法是年份+月份，Ubuntu 04.10（2004年10月）。

LTS版本（Long Term Support），长期支持版，LTS版本至少提供4年的系统更新服务，而普通的版本只提供半年的更新服务。所以一般来说，很多人选择使用LTS版本。

LAMP
-----

LAMP并不是一个软件，它是经过多年的Web技术发展，在业内被广泛使用的一种Web服务器解决方案之一（LNMP也非常受欢迎），由一些独立的系统或软件组合而成。通常认为，Linux＋Apache＋MySql＋PHP。并非只有Apache可以通过扩展支持PHP的解析，Nginx，LightHttpd等其它软件同样可以。

LAMP工作原理:

Ubuntu管理员权限解读：

为了安全，Ubuntu官方不推荐使用root账户远程登陆，在系统安装过程中，系统会强制要求设置一个普通用户。
普通账户没有管理员权限。
默认情况下root账户无法登陆，默认密码为空，为空不能登陆。
su（Switch User）切换到超级管理员，当前用户身份完全切换到root账户，使用root账户密码登录，除非执行exit退出登录，否则超级权限将一直有效。
sudo（Switch User and DO）以超级管理员身份执行，当前用户身份没有改变，使用自身密码获取授权，超级权限是临时的。
sudo弥补了su产生的多账户安全问题，使用su命令所有管理员都必须知道root账户的密码，sudo使得普通管理员使用自己的密码也可以获得超级管理员权限。

命令行：用户名@主机名:当前目录 用户类型标记，$表示普通用户，#表示超级管理员

通过passwd命令修改账户密码：sudo passwd root。
Passwd命令必须拥有系统超级权限才可以执行，所以当使用非root账户登录系统时执行passwd命令必须在命令前加上sudo前缀，使用root账户登陆服务器时已经拥有了超级权限，执行passwd命令时无需加sudo前缀。

apt-get 安装软件

apt-get update 更新软件源列表
apt-get install 安装软件

LNMP
-----