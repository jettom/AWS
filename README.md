# Related knowledges

## VPC

### 概述

1. [官方文档](https://docs.aws.amazon.com/zh_cn/vpc/latest/userguide/what-is-amazon-vpc.html)

### CIDR

[CIDR计算器](http://www.subnet-calculator.com/cidr.php)

### 相关习题

1. 一家公司需要记录私有子网中所有IP包（源，目标，协议），最佳解决方案是什么？（#1-8）
   - [ ] A. 使用[VPC flow logs](https://docs.aws.amazon.com/zh_cn/vpc/latest/userguide/flow-logs.html)。
   - [ ] B. 使用EC2上的`source destination checkout`。
   - [ ] C. 使用[AWS CloudTrail](https://docs.aws.amazon.com/zh_cn/awscloudtrail/latest/userguide/cloudtrail-user-guide.html)并且使用S3存储日志文件。
   - [ ] D. 使用[Amazon CloudWatch](https://docs.aws.amazon.com/zh_cn/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html)进行监控
   
2. 一个应用运行在私有子网的EC2实例上，这个应用需要读写`Amazon Kinesis Data Streams`上的数据。但是该公司要求读取数据的流不能流向万维网（Internet），怎样实现一上需求？（#1-39）
   - [ ] A. 在一个共有子网中配置一个[NAT网关（NAT Gateway）](https://docs.aws.amazon.com/zh_cn/vpc/latest/userguide/vpc-nat-gateway.html)并且将读写流路由到`Kinesis`服务上。
   - [ ] B. 为`Kinesis`配置一个[网关 VPC 终端节点（Gateway VPC Endpoint）](https://docs.aws.amazon.com/zh_cn/vpc/latest/userguide/vpce-gateway.html)并且通过其将读写流路由到`Kinesis`服务上。
   - [ ] C. 为`Kinesis`配置一个[接口 VPC 终端节点（Interface VPC Endpoint）](https://docs.aws.amazon.com/zh_cn/vpc/latest/userguide/vpce-interface.html)并且通过其将读写流路由到`Kinesis`服务上。
   - [ ] D. 为`Kinesis`配置一个[AWS Direct Connect 虚拟接口](https://docs.aws.amazon.com/zh_cn/directconnect/latest/UserGuide/WorkingWithVirtualInterfaces.html)并且通过其将读写流路由到`Kinesis`服务上。

## AWS Outposts

### 概述

AWS Outposts 是一项完全托管的服务，可将 AWS 基础设施、AWS 服务、API 和工具扩展到几乎任何数据中心、共处空间或本地设施，以实现真正一致的混合体验。AWS Outposts 非常适合**需要低延迟访问本地系统、本地数据处理或本地数据存储的工作负载**。

### 应用

AWS Outposts 解决了多种行业中的低延迟应用程序需求和本地数据处理需求。
