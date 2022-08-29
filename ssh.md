## ssh 专辑

在 centos7 下重启服务不再是 service 服务名称 动作 这样的方式的.而是:

```bash
systemctl 动作 服务名.service
```

```bash
#1. 查看sshd服务是否启动了.
systemctl status sshd.service
#2. 如果没有启动,则需要启动该服务:
systemctl start sshd.service
#3. 如果需要重启sshd服务可使得
systemctl restart sshd.service
#4. 设置为开机启动可使用:
systemctl enable sshd.service
```

### 关于权限

> ssh rejects key-based logins if permissions allow other people to tamper with your authorized_keys file. You need to check /, /home, /home/yourname, /home/yourname/.ssh and /home/yourname/.ssh/authorized_keys. All of those must not be group or world writeable.
> .ssh 和 authorized_keys 的权限应该是 755，这样可以避免其他软件篡改
