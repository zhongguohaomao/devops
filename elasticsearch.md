## download
```
cd /codeyuguo/elasticsearch
wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-6.7.1.tar.gz
tar -xzvf elasticsearch-6.7.1.tar.gz
mv elasticsearch-6.7.1 elasticsearch

```
## add new user add give elasticsearch dir power
```
passadd elasticsearch
passwd elasticsearch
chown elasticsearch /codeyuguo/elasticsearch -R

```

## modify elasticsearch config
```
cd /codeyuguo/elasticsearch/elasticsearch/config
vi elasticsearch.yml
#添加如下配置
cluster.name: codeyuguo-es
node.name: master-002
path.data: /codeyuguo/elasticsearch/data
path.logs: /codeyuguo/elasticsearch/logs
network.host: 192.168.5.116
transport.tcp.port: 9300 
http.port: 9200
discovery.zen.ping.unicast.hosts: ["192.168.5.116", "192.168.6.49", "192.168.15.90"]

```

## modify vm.max_map_count
```
vi /etc/sysctl.conf
#添加如下配置
vm.max_map_count=262144
sysctl -p

```

## start elasticsearch
```
cd /codeyuguo/elasticsearch/elasticsearch/bin
su elasticsearch
./elasticsearch -d
ps -ef|grep elasticsearch
网页访问192.168.5.116:9200
其余实例方法相同
```