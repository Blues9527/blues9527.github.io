1.初次创建需要新建一个repository仓库，然后仓库的名称是 <Github名称>.github.io，==注意不能是其他的==

2.将repository 克隆到本地，然后招一套theme替换掉如：
![githubpages.png](http://note.youdao.com/yws/res/15526/WEBRESOURCEc5eabc0469e0d26f7e190ac13e784698)

3.使用脚本安装jekyll，脚本命令如下，sudo主要是防止没有权限安装

```
sudo gem install jekyll
```

4.安装完后切换到仓库目录

```
bundle install
```

5.执行完上述命令之后，执行jekyll

```
bundle exec jekyll serve
```

6.开启后访问 127.0.0.1:4000可以看到预览效果

7.修改_config.yml文件去修改博客信息

8.提交blog必须是要md格式，且要命名为yyyy-MM-dd- filename.md，否则无法预览

9.git相关操作
```
git init

git clone repositoryUrl localDirUrl

git add --all

git commit -m "日志"

git push origin master
```

10.有道云地址（http://note.youdao.com/noteshare?id=eec41462c99bf199def8c32554a51921）

