WHMCS插件   https://github.com/hackenwu/V2raySocks

安装git

# Centos安装
yum install git -y

# Ubuntu安装
apt-get install git

# 拉取后端
git clone https://github.com/hackenwu/V2/

# 给予可执行权限
cd V2
chmod -R 777 *

# 安装v2ray
./go.sh
---------------------------------------------------
# 修改数据库信息
vi config.json
-----------------------------------------------------
 # 修改v2ray.json
vi v2ray.json

-----------------------------------------------------
# 运行测试
./main

确认无错误后，丢到后台运行：

# 先停止运行
# Ctrl+C键
# 使用screen，将这个进程挂起。

# 安装screen
# Centos命令
yum install screen -y

# Ubuntu命令( ubuntu默认已经安装
apt-get install screen

# 新建screen进程
screen -S v2
# 这个命令后 会跳转一个空白页面，

# 接着输入
./main

# 同样确认无错后同时按Ctrl+A 松开 再按一下D键  即可！





