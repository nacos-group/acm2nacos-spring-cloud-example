
本仓库旨在给spring-cloud-alibaba用户提供acm迁移nacos的能跑通的demo。

在整个迁移过程中，用户只需要做两部操作：

1 参考https://help.aliyun.com/document_detail/312705.html  将配置从acm导出，并导入到nacos

2 在src/main/resources目录下的bootstrap.properties下面进行如注释内容的替换。

```

# 配置中心的endpoint。
# 在ACM迁移MSE Nacos的过程中，需要将这个{endpoint}替换为MSE Nacos的内网/外网地址。（可以在MSE Nacos集群的详情页的"基础信息"栏目中找到）
spring.cloud.nacos.config.endpoint={endpoint}
# 注册中心的namespace。
# 在ACM迁移MSE Nacos的过程中，需要在MSE Nacos集群的详情页的"命名空间"栏目中新建namespace，并且将namespace id复制到{namespace}处。
# 您也可以选择使用默认的namespace，如果使用默认的"public"的namcespace,请不要填写这个值，直接留空即可。
spring.cloud.nacos.config.namespace={namespace}
# AK和SK信息，在ACM迁移Nacos过程中不需要更改。
spring.cloud.nacos.config.access-key={ak}
spring.cloud.nacos.config.secret-key={sk}

```
