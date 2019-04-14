# 1、源码的拉取和环境搭建
当前master版本为2.7.2

从官方fork仓库到自己的GitHub仓库[](https://github.com/lishuai2016/incubator-dubbo),然后构建自己的分支
[ls_from_master_20190414]

下载到自己电脑中，然后使用idea打开，然后使用clean package -Dmaven.test.skip=true
跳过测试部分打包，在打包的过程中回去下载所依赖的jar包。




## 遇到的问题
1、使用multicast registry方式找不到服务注册者，替换本地的zookeeper后demo运行成功
模块：[dubbo-demo-api-provider]
模块：[dubbo-demo-api-consumer]

服务提供者:service.setRegistry(new RegistryConfig("zookeeper://127.0.0.1:2181"));
服务消费者：reference.setRegistry(new RegistryConfig("zookeeper://127.0.0.1:2181"));

