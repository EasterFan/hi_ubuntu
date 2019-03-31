> 安装nvm-----配置nvm环境变量----安装node ----淘宝cnpm加速

## 一. 安装 nvm
nvm是一个开源的 Node 版本管理器，通过简单的 bash 脚本来管理、切换多个 Node.js 版本,使用 nvm 可以安装官网最新版本之前的任意版本,可以任意切换不同版本  

下载：  
```bash
git clone https://github.com/creationix/nvm.git ~/.nvm && cd ~/.nvm && git checkout `git describe --abbrev=0 --tags`  
```
配置环境变量：  
```bash
# 打开文件
vim ~/.bashrc
# 加入位置
source ~/.nvm/nvm.sh
export NVM_DIR="/Users/YOURUSERNAME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"  # This loads nvm
# 检验
source  .bashrc 
nvm --version
```

## 二. 安装 node
```bash
# 查找 node 版本
nvm ls-remote
# 安装node版本并设为默认node
nvm install 8.10.0
nvm alias default 8.10.0
# 检验
node --version
npm -v

# 查看已安装的node
nvm ls
# 切换 node 版本
nvm use 8.10.0
# 卸载node
nvm uninstall 8.10.0
```
node 8.10.0对应的npm 是5.6.0？？

## 三.淘宝 cnpm 加速
```bash
# 下载
npm install -g cnpm --registry=https://registry.npm.taobao.org
# 验证
cnpm -v
```
[淘宝npm镜像](http://npm.taobao.org/)

