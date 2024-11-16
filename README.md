# 微服务项目练习

#### 服务注册与发现(Consul, Nacos)
#### 服务调用和负载均衡(LoadBalancer, OpenFeign)
#### 服务链路追踪(Micrometer Tracing)

#### 熔断和限流（CircuitBreak、Sentinel）  配置在调用方

#### 服务网关(Gateway)   路由、断言、过滤
#### 分布式配置管理(Consul, Nacos)
#### 分布式事务(Seata)

consul启动地址：http://localhost:8500/

consul注册中心和配置中心、配置中心的持久化

config/{spring.application.name}{分隔符}{profile}/data   对应的config/cloud-payment-service-dev/data

zipkin链路追踪 （配置在被调用方的）   java-jar启动   需要jdk17   http://localhost:9411/api/v2/spans



-----

nacos的安装配置：

+ 安装包里的sql先导到数据库，修改application.properties配置数据库的连接

+ `nacos\bin> .\startup.cmd -m standalone`

sentinel有两个端口，运行端口8719和控制台端口8080，sentinel一般跟网关整合

```yaml
        dashboard: localhost:8080
        port: 8719 # 默认端口
```



seata需要配置注册中心将自己注册进去，还需要配置数据库连接





根据([尚硅谷2024最新SpringCloud教程，springcloud从入门到大牛](https://www.bilibili.com/video/BV1gW421P7RD/?share_source=copy_web&vd_source=2fda0b25e50e841c8126929ff3e47259))视频练习 <br>

[本项目sql文件](resource/sql) <br>
需要多个实例请自己修改端口号启动 `-Dserver.port=9002`
