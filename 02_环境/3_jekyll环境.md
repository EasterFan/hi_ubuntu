> github pages 托管的静态博客，我的：[https://easterland.me/](https://easterland.me/)

## 1. 安装 `ruby-install`
```bash
wget -O ruby-install-0.6.1.tar.gz https://github.com/postmodern/ruby-install/archive/v0.6.1.tar.gz
tar -xzvf ruby-install-0.6.1.tar.gz
cd ruby-install-0.6.1/
sudo make install
```

## 2. 安装 ruby
```bash
# 过程漫长
sudo ruby-install --system ruby
# 检验
ruby -v
```

## 3. 安装 `jekyll`
```bash
# jekyll要在ruby2.0以上的版本才能安装成功
sudo gem install jekyll
# 验证
jekyll --help
```

## 4. 安装bundler
> jekyll的运行依赖bundler包

```bash
sudo gem install bundler
# 验证
jekyll new blog
```
至此，jekyll环境已经安装完成，进入博客仓库，运行

```bash
bundle install
npm start
```
