## 用户管理

### 创建用户并授予可无密码执行 sudo 命令

```
#创建一个work用户用来部署应用
#使用root用户登陆，将下面这行配置放到/etc/sudoers 中的root下
work ALL = NOPASSWD: /bin/systemctl restart httpd.service, /bin/kill

```

这种方法适合人肉运维的情况。如果是大集团的机器，权限应该划分更加清晰。用于部署应用的 work 用户不应该拥有修改系统设置的权限。容器化部署的情况下一个 docker 的权限足矣。
https://www.cyberciti.biz/faq/linux-unix-running-sudo-command-without-a-password/
