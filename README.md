# 安装git

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

# 示例：
{
    "Mysql_Host": "数据库地址",
    "Mysql_Port": 3306,
    "Mysql_User": "数据库用户名",
    "Mysql_Password": "数据库密码",
    "Mysql_Db": "数据库表",
    "Mysql_TLS": "false",
    "Mysql_MaxOpenConns": 100,
    "Mysql_MaxIdleConns": 10,
    "V2rayClientAddr": "127.0.0.1:8301",
    "V2rayTag": "proxy",
    "Email": "@test.com",
    "AlterID": 64,
    "Level": 1,
    "CheckRate": 64
}

-----------------------------------------------------
 # 修改v2ray.json
vi v2ray.json

 "inbound": {
    "port": 10086,   # 监听端口随便，对应上面Nginx 的端口   
    "protocol": "vmess",
    "settings": {
      "clients": []
    },
    "streamSettings": {
      "network": "ws" # 这里是whmcs > 产品管理 > 模块设置 > 线路列表中的 “传输协议” 必须一致
   "wsSettings": { "path":"/ray" } # 添加
    },

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





