> gitbook 需要 node 环境

## 一. 安装 gitbook
```bash
# 安装
cnpm install gitbook-cli -g
# 检验 -- 时间较长
gitbook -V
```

一些其他操作  
```bash
# 列出远程所有可用版本

gitbook ls-remote

# 列出本地所有已安装版本

gitbook ls

# 卸载本地某版本

gitbook uninstall x.x.x
```
## 二. 安装 gibook 插件
> 自动生成 summary 文件

```bash
# 安装
npm install -g gitbook-summary

# 启动
book sm
```
[npm 插件](https://www.npmjs.com/package/gitbook-summary)  

github-pages 一键发布插件
```
npm install -g gh-pages
gh-pages -d _book
```


## 三. 安装 atom
### 1. 下载
[下载](https://atom-installer.github.com/v1.24.1/atom-amd64.deb?s=1520526466&ext=.deb)  

### 2. 安装插件
表格功能： atom-csv-markdown  
粘贴图片改路径：Markdown-img-paste -- 在 settings 中设置图片路径(超级喜欢，可是作者不维护了～)  
同步预览：markdown-scroll-sync
