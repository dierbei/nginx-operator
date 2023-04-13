# nginx-operator
operator-sdk develop nginx operator

## operator-sdk 版本支持
```text
1.24 支持 go1.18
```

## 初始化项目结构
```shell
# 这个命令设置了许多不同的文件和文件夹，这些文件和文件夹将用我们正在构建的操作符的自定义 API 和逻辑填充。
operator-sdk init --domain hedui.com --repo github.com/dierbei/nginx-operator

# config --- 保存 operator 资源定义
# hack   --- 脚本目录
# .dockerignore --- Docker 将忽略的文件的声明性列表
# Dockerfile --- 构建容器
# Makefile --- operator 构建定义
# go.mod --- 依赖
# main.go --- operator 主函数入口点
```
