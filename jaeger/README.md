## elastic 作为后端

参照：
https://my.oschina.net/u/2548090/blog/1821372


## cassandra 作为后端

1. 下载jaeger
git clone https://github.com/jaegertracing/jaeger.git

2. 进入jaeger的脚本目录
cd jaeger/plugin/storage/cassandra/schema

3. 设置环境变量
export DATACENTER=dc1
export KEYSPACE=jaeger_v1

4.初始化cassandra表结构
docker run --rm \
  --name jaeger-cassandra-schema \
  -e MODE=prod \
  -e CQLSH_HOST=120.26.72.91 \
  -e KEYSPACE=jaeger_v1 \
  jaegertracing/jaeger-cassandra-schema



## 参照资料
https://xenojoshua.com//2019/04/jaeger-note/#51-metrics

官方文档
https://www.jaegertracing.io/docs/1.19/deployment/#cassandra
