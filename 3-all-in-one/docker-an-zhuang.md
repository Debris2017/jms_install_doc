Docker 安装见:[Docker官方安装文档](https://docs.docker.com/install/)

## 快速启动

使用 root 命令行输入:

```
$ docker run -d -p 8080:80 -p 2222:2222 registry.jumpserver.org/public/jumpserver:1.0.0
```

## 访问

浏览器访问:[http:/](http://docs.jumpserver.org/)/&lt;容器所在服务器IP&gt;:80

SSH访问: ssh -p 2222 &lt;容器所在服务器IP&gt;

XShell等工具请添加connection连接

## 额外环境变量

* DB\_ENGINE = mysql
* DB\_HOST = mysql\_host
* DB\_PORT = 3306
* DB\_USER = xxx
* DB\_PASSWORD = xxxx
* DB\_NAME = jumpserver
* REDIS\_HOST = &lt;redis-host&gt;
* REDIS\_PORT = &lt;redis-port&gt;
* REDIS\_PASSWORD = &lt; &gt;

```
docker run -d -p 8080:80 -p 2222:2222 -e DB_ENGINE=mysql -e DB_HOST=192.168.1.1 -e DB_PORT=3306 -e DB_USER=root -e DB_PASSWORD=xxx -e DB_NAME=jumpserver  registry.jumpserver.org/public/jumpserver:1.0.0
```

## 仓库地址

[https://github.com/jumpserver/Dockerfile](https://github.com/jumpserver/Dockerfile)

