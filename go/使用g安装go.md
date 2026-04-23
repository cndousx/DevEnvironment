# 使用g安装go


1. [下载g](https://github.com/voidint/g/releases)解压到指定目录，然后将j所在目录添加到环境变量中
2. 运行`g install 1.26.2`安装指定版本
3. 运行`g use 1.26.2`切换指定版本
4. 运行`g ls`查看已安装的版本
5. g默认将go安装到当前用户下的.g目录下。使用g use 切换的是`HOME/.g/go`，将.g/go配置到环境变量中，方便使用`go`命令

