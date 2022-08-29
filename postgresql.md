## Postgresql

### 安装

```
# 来自 https://www.postgresql.org/download/linux/redhat/
sudo yum install -y https://download.postgresql.org/pub/repos/yum/reporpms/EL-7-x86_64/pgdg-redhat-repo-latest.noarch.rpm
sudo yum install -y postgresql14-server
sudo /usr/pgsql-14/bin/postgresql-14-setup initdb
sudo systemctl enable postgresql-14
sudo systemctl start postgresql-14
```

### 修改默认密码

https://chartio.com/resources/tutorials/how-to-set-the-default-user-password-in-postgresql/
