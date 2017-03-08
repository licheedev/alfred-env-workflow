# alfred-env-workflow
Alfred 3 Workflow——加载环境变量并运行mac应用

解决mac上直接运行app，出现找不到环境变量，找不到文件或命令的问题。

# 下载

[**Run App with ENV (bash ver).alfredworkflow**](https://github.com/licheedev/alfred-env-workflow/raw/master/Run%20App%20with%20ENV%20(bash%20ver).alfredworkflow)

[**Run App with ENV (zsh ver).alfredworkflow**](https://github.com/licheedev/alfred-env-workflow/raw/master/Run%20App%20with%20ENV%20(zsh%20ver).alfredworkflow)

# 使用

> env 应用关键字

# 示例

![演示](https://raw.githubusercontent.com/licheedev/alfred-env-workflow/master/images/3.gif)

# 制作动机

最近发现 mac 上面的app，直接点击图标运行，是不会加载 shell 配置好的环境变量的。

比如Android Studio导入项目时找不到 `ANDROID_HOME` ，

![ANDROID_HOME](https://raw.githubusercontent.com/licheedev/alfred-env-workflow/master/images/1.jpg)

SourceTree无法通过 [connect](https://bitbucket.org/gotoh/connect/wiki/Home) SSH代理克隆项目，

![SourceTree无法使用SSH代理](https://raw.githubusercontent.com/licheedev/alfred-env-workflow/master/images/2.jpg)

如果通过终端 `open app` 来运行应用，结果都没问题，看来是环境变量的问题。

于是试着搞了个 Alfred Workflow ，先 `source ~/.bash_profile` 导入环境变量，再 `open` 应用，效果不错。
