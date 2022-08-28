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
