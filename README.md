# cwgo-template

## 项目介绍

参考云原生最佳实践，对 cwgo 的 rpc server 标准模板进行了优化

* docker 镜像构建
* 系统配置通过环境变量传入
* 日志输出到控制台

## 使用方式

在原有的生成命令末尾添加 `--template https://github.com/suyiiyii/cwgo-template.git` 参数

```shell
cwgo server --type RPC ... --template https://github.com/suyiiyii/cwgo-template.git
``` 

## 详细更改

在原来的基础上添加了

* Dockerfile 模板
* gorm 模型模板
* gorm gen 模板

在原来的基础上重构了

* 移除多环境配置文件，改为使用 viper 管理的单一配置文件，内嵌到二进制文件，并支持环境变量覆盖
* 移除文件日志，改为直接打印到控制台
* 数据库使用 mysql 并且添加自动创建数据库功能

## 参考

https://www.cloudwego.io/zh/docs/cwgo/tutorials/templete-extension/