# go mod

go mod download 下载模块到本地缓存，缓存路径是 $GOPATH/pkg/mod/cache
go mod edit 是提供了命令版编辑 go.mod 的功能，例如 go mod edit -fmt go.mod 会格式化go.mod
go mod graph 把模块之间的依赖图显示出来
go mod init 初始化模块（例如把原本dep管理的依赖关系转换过来）
go mod tidy 增加缺失的包，移除没用的包
go mod vendor 把依赖拷贝到 vendor/ 目录下
go mod verify 确认依赖关系
go mod why 解释为什么需要包和模块



