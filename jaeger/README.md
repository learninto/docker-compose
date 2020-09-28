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
sh ./create.sh | cqlsh 120.26.72.91
