## Python

比较粗糙的方法是`yum install -y python`，但是这样的版本不可控. centos7.6 上是 3.6，而 docker-compose 只支持 3.7 及以后，所以需要手动安装。

### python 安装包

- 官方各版本下载地址：https://www.python.org/ftp/python/
- 华为镜像：https://mirrors.huaweicloud.com/python/

### pip mirrors

- 豆瓣 https://pypi.douban.com/simple
- 阿里云 https://mirrors.aliyun.com/pypi/simple
- 清华大学 https://pypi.tuna.tsinghua.edu.cn/simple
- 中国科技大学 https://pypi.mirrors.ustc.edu.cn/simple

```
pip install pandas -i https://mirrors.aliyun.com/pypi/simple
```

### 安装

#### 下载安装包

```
cd /usr/src
wget https://mirrors.huaweicloud.com/python/3.7.11/Python-3.7.11.tgz
Now extract the downloaded package.
```

#### 解压

```
tar xzf Python-3.7.11.tgz
```

#### 安装

```
cd Python-3.7.11
./configure --enable-optimizations
make altinstall #防止替换默认的/usr/bin/python.
```

#### 打扫战场

```
rm /usr/src/Python-3.7.11.tgz
# 替换python3命令，如果原来没有用-s选项即可
sudo ln -snf /usr/local/bin/pip3.7 /usr/bin/pip3
sudo ln -snf /usr/local/bin/python3.7 /usr/bin/python3
```

#### 善刀而藏

```
python3.7 -V
```

### Reference:

https://tecadmin.net/install-python-3-7-on-centos/
