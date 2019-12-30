##rocketmq项目结构

####
+ rocketmq-broker：接受生产者发来的消息并存储（通过调用rocketmq-store），消费者从这里取得消息
+ rocketmq-client：提供发送、接受消息的客户端API。
+ rocketmq-namesrv：NameServer，类似于Zookeeper，这里保存着消息的TopicName，队列等运行时的元信息。
+ rocketmq-common：通用的一些类，方法，数据结构等。
+ rocketmq-remoting：基于Netty4的client/server + fastjson序列化 + 自定义二进制协议。
+ rocketmq-store：消息、索引存储等。
+ rocketmq-filtersrv：消息过滤器Server，需要注意的是，要实现这种过滤，需要上传代码到MQ！（一般而言，我们利用Tag足以满足大部分的过滤需求，如果更灵活更复杂的过滤需求，可以考虑filtersrv组件）。
+ rocketmq-tools：命令行工具。

