# cwgo-template

在原来的基础上添加了
* Dockerfile 模板
* gorm 模型模板
* gorm gen 模板

在原来的基础上重构了
* 移除多环境配置文件，改为使用 viper 管理的单一配置文件，支持环境变量覆盖
* 移除文件日志，改为直接打印到控制台
