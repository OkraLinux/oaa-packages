OAA packages

OkraLinux aarch64 基础软件包的构建产物

packages 目录是配方，scripts 是构建脚本，out 是编译好的 oaa 和校验文件

这些包由 ylh440104/okra-oaa-build 的 actions 自动推过来

安装时用 lunar 或者 oaa 指向 out 里的文件

软件源服务器可以直接把 out 目录当 artifacts 用
