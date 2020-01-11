### 搭建dns服务器

```
docker run -d --name dns --restart=always -p 5380:8080 -p 53:53/tcp -p 53:53/udp -e TZ='Asia/Shanghai' -e HTTP_USER='root' -e HTTP_PASS='00000' 964973791/dns:latest
```

### 添加解析

```
[root@localhost ~]# cat /etc/resolv.conf
nameserver 127.0.0.1
```

### 登陆

```
http://172.27.0.1:5380
```

### 用户/密码

```
user:   root
passwd: 00000
```

