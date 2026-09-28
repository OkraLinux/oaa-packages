OAA packages

OkraLinux aarch64 基础软件包的构建产物

packages 是配方，scripts 是构建脚本，out 是编译好的 oaa

out 里每个包三份文件，oaa 本体，sha256 校验，sources 记源码地址和哈希

重新构建任意一个包

    bash scripts/build-package.sh grep

必须在 aarch64 的 linux 上跑，因为产物就是 aarch64 原生的，x86 机器上编译不出来

加包就在 packages 里加一个 conf，脚本会自动收集，不用改别的地方

依赖关系写在 conf 的 Dependencies 里，现在都是依赖 glibc

这一批是补齐基础系统缺的工具，kmod 和 libseccomp 补上以后 systemd 的报错会少很多

源码没有放进仓库，只存地址和 sha256，要归档的话把 sources 里的 tar 包拉下来就行
