## Newbee SRE 的一些脚本

> 机器一般从裸机开始。一直在用 centos7.6。

### Java、Node、Python 一把梭哈，一些基础包

```
sudo yum -y install git maven java-11-openjdk python3 npm

```

### 🇨🇳 中国大陆一键安装 oh-my-zsh

```bash
#oh-my-zsh 中国大陆你懂的原因。服务器不像开发机器没必要上代理，代理未必稳定还可能弄乱网络直连、代理规则。多一事不如少一事。
#基于 https://github.com/ohmyzsh/ohmyzsh#manual-installation 整理改编
sudo yum install -y git zsh
git clone https://gitee.com/mirrors/oh-my-zsh.git ~/.oh-my-zsh
cp ~/.zshrc ~/.zshrc.orig
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
chsh -s $(which zsh)
# 有时候chsh列表中的zsh和which zsh的值不一致，试试下面的命令
chsh -s $(chsh -l|grep zsh)
#接下来重启下shell就可以了。直接exit退出当前ssh session也可
```
