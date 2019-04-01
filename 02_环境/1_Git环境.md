## 安装 Git 并升级至最新版
```bash
sudo apt-get install git
sudo add-apt-repository ppa:git-core/ppa
sudo apt update
sudo apt install git

# 检验
git --version
```

## SSH密钥配置
> 配置后不需要总输入密码

1. 生成密钥 - -f指定位置和名称
```bash
# 生成密钥
ssh-keygen -t rsa -C "xxxx@gmail.com" -f ~/.ssh/test_github
（遇到过 ssh 每过一段时间就失效的问题，用下面的步骤，一般用上面一个就够了）
# 确认ssh-agent处于启用状态 -- 输出 PID
eval "$(ssh-agent -s)"
# 将SSH key添加到ssh-agent
ssh-add ~/.ssh/test_github
# 测试连接
ssh -vT git@github.com
```

2. 复制公钥  
将test-github.pub文件的内容添加到github的“SSH KEYS”里面


## 导入 .gitconfig
> 包含个人信息和别名配置

先进入`cd ~/.gitconfig`,再修改
```bash
[user]
    email = xxxx@gmail.com
    name = EasterFan



[alias]
    ci = commit
    st = status
    hi = log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short
    pu = push origin master
```
