
# 安装Redis
```
cd ~
wget http://download.redis.io/releases/redis-5.0.0.tar.gz
tar -zxvf redis-5.0.0.tar.gz
cd redis-5.0.0
make
make install 
cd utils 
sudo ./install_server
rm redis-5.0.0.tar.gz
rm -r redis-5.0.0

```
# 安装  mongodb
```
1.
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 9DA31620334BD75D9DCB49F368818C72E52529D4


2.
# 16,04
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/4.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.0.list
#18.04
echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.0.list


3.
sudo apt-get update

4.
sudo apt-get install -y mongodb-org


```

# 安装 maraidb
```
curl -sS https://downloads.mariadb.com/MariaDB/mariadb_repo_setup | sudo bash
sudo apt update 
sudo apt install mariadb-server-10.3

```


# 安装 Docker

## https://blog.csdn.net/qq_36148847/article/details/79273591

```

1.如果以前安装过老版本，可以先卸载以前版本
sudo apt-get remove docker docker-engine

2.安装 docker-ce 和密钥管理以及下载相关的工具
sudo apt-get install apt-transport-https ca-certificates curl python-software-properties software-properties-common

3.下载并安装密钥
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -

4.查看密钥是否安装成功 
sudo apt-key fingerprint 0EBFCD88

5.添加 docker 官方仓库
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian wheezy stable"

６.更新仓库
sudo apt-get update


7.安装 docker-ce 
sudo apt-get install docker-ce

8.启动 docker-ce
systemctl start docker


9.将当前用户加入docker用户组
sudo gpasswd -a ${USER} docker  
sudo chmod a+rw /var/run/docker.sock

```

