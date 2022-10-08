## rocketmq拉取消息为什么采用长轮询的策略？

如果broker没有消息，短轮询会因为消费者频繁连接broker而浪费网络带宽资源。此时如果连接保持一段时间，如果此时收到消息，则立刻返回。超时后也返回，就避免了频繁连接。

## rocketmq的nameserver为什么不使用zookeeper？

因为只需要保存元数据信息，不需要选举。
