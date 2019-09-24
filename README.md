# 安装

## RVM 安装

[RVM](https://rvm.io/) 是一个命令行工具，可以提供一个便捷的多版本 Ruby 环境的管理和切换。

如果你打算学习 Ruby / Rails, RVM 是必不可少的工具之一.

```text
$ gpg --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3  7D2BAF1CF37B13E2069D6956105BD0E739499BDB
$ \curl -sSL https://get.rvm.io | bash -s stable
$ source ~/.bashrc
$ source ~/.bash_profile
$  source /etc/profile.d/rvm.sh
```

   检查一下是否安装正确

```ruby
$ rvm -v
```

## 用 RVM 安装 Ruby 环境

修改 RVM 下载 Ruby 的源，到 Ruby China 的镜像

```text
echo "ruby_url=https://cache.ruby-china.com/pub/ruby" > ~/.rvm/user/db
```

列出已知的 ruby 版本

```text
$ rvm list known
```

可以选择现有的 rvm 版本来进行安装

```text
$ rvm install 6.0.0
```

等待一会便可安装成功，时间可能有点长。

查询已经安装的 ruby和卸载ruby

```text
$ rvm list
$ rvm remove 6.0.0  #必须是使用rvm install 安装的版本
```

### 设置 Ruby 版本 <a id="&#x6B65;&#x9AA4;3 &#xFF0D; &#x8BBE;&#x7F6E; Ruby &#x7248;&#x672C;"></a>

RVM 装好以后，需要执行下面的命令将指定版本的 Ruby 设置为系统默认版本

```text
$ rvm 6.0.0 --default
```

同样，也可以用其他版本号，但一定是用rvm install 安装过那个版本

这个时候你可以测试是否正确

```text
$ ruby -v
ruby 6.0.0 ...
```

### 安装 Rails 环境 <a id="&#x6B65;&#x9AA4;4 &#xFF0D; &#x5B89;&#x88C5; Rails &#x73AF;&#x5883;"></a>

上面 3几个步骤过后，Ruby 环境就安装好了，接下来安装 Rails

```text
$ gem install rails
```

然后测试安装是否正确

```text
$ rails -v
Rails 4.2.5
```
### Windows安装 
 [点击这里下载](https://rubyinstaller.org/downloads/)
 
 * 下载 rubyinstaller 之后，解压到新创建的目录下
 * 双击 rubyinstaller-2.2.3.exe 文件，启动 Ruby 安装向导。
 * 点击 Next，继续向导，记得勾选 `Add Ruby executables to your PATH`直到 Ruby 安装程序完成 Ruby 安装为止。

完。

