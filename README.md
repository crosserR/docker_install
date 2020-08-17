# docker_install
docker一键安装脚本（全平台，懒人必备）

```
sudo wget -qO- https://get.docker.com/ | bash
```

# 或者
```
curl -fsSL https://get.docker.com -o get-docker.sh && sudo sh get-docker.sh
```

# 安装成功执行下面语句，如果有类似回显，说明安装成功

```
$ docker --version
Docker version 18.06.1-ce, build e68fc7a
```

# Ubuntu 16.04+、Debian 8+、CentOS 7
#### 国内从 Docker Hub 拉取镜像有时会遇到困难，此时可以配置镜像加速器。国内很多云服务商都提供了国内加速器服务，例如：
```
网易云加速器 https://hub-mirror.c.163.com
百度云加速器 https://mirror.baidubce.com
```
#### 由于镜像服务可能出现宕机，建议同时配置多个镜像。
##### 本节我们以 网易云 镜像服务 https://hub-mirror.c.163.com 为例进行介绍。
对于使用 systemd 的系统，请在 /etc/docker/daemon.json 中写入如下内容（如果文件不存在请新建该文件）
```
{
  "registry-mirrors": [
    "https://hub-mirror.c.163.com",
    "https://mirror.baidubce.com"
  ]
}
```
之后重新启动服务。
```
$ sudo systemctl daemon-reload
$ sudo systemctl restart docker
```
# 完成
