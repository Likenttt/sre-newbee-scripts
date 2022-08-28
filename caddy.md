## caddy - 替代 nginx

最明显的优势就是 caddy 的配置文件不那么吓人。作为一个非常 newbee 的 sre，一个简单的 proxy_pass nginx 的长篇累牍指令不免有点令人生畏。caddy 还集成了 ssl 证书 ca 的一些功能，申请证书非常便捷友好。

### 安装

```
sudo yum install -y caddy

```

### 一个简单的配置文件 caddyfile

```
https://li2niu.com {
    reverse_proxy localhost:6000
}
```

### 启动

```
caddy start --config /root/caddyfile --adapter caddyfile
```

### caddy 缺点是什么

性能比 nginx 稍稍差一些，配置文件不像 nginx 那样可以随意搜寻借鉴。
有点像 python 和 java 的差别。很多时候 python 用起来还是很方便的。
