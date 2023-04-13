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

## 初始化 API
```shell
operator-sdk create api --group operator --version v1alpha1 --kind NginxOperator --resource --controller

# 1. Creates the API types in a new directory called api/

# 2. Defines these types as belonging to the API group operator.hedui.com (since we initialized the project under the domain hedui.com)

# 3. Creates the initial version of the API named v1alpha1

# 4. Names these types after our Operator, NginxOperator

# 5. Instantiates boilerplate controller code under a new directory called controllers/ (which we will work with more under Writing a control loop)

# 6. Updates main.go to add boilerplate code for starting the new controller
```