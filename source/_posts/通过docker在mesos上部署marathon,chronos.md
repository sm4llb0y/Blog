title: 通过docker在mesos上部署marathon,chronos
date: 2016-04-07 11:58:31
tags: Docker, Mesos, Zookeeper, Marathon, Chronos
---

1. 首先查看IP，通常IP地址应该是172.17.42.1
```bash
ip route | grep docker | awk '{ print $NF }'
```
2. 运行Zookeeper
```bash
docker run -d -p 2181:2181 -p 2888:2888 -p 3888:3888 jplock/zookeeper
```
3. 运行Mesos Master
```bash
docker run -d -e MESOS_LOG_DIR=/var/log \
 -e MESOS_WORK_DIR=/var/log \
 -e MESOS_ZK=zk://172.17.42.1:2181/mesos \
 -e MESOS_HOSTNAME=172.17.42.1 \
 -e MESOS_QUORUM=1 \
 -p 5050:5050 \
 redjack/mesos-master
```
4. 运行Mesos Slave
```bash
docker run -d \
 -e MESOS_LOG_DIR=/var/log \
 -e MESOS_MASTER=zk://172.17.42.1:2181/mesos \
 -e MESOS_HOSTNAME=172.17.42.1 \
 -p 5051:5051 \
 -p 31800:31800 \
 redjack/mesos-slave
```
5. 运行Marathon
```bash
docker run -p 8088:8088 -d -t mesosphere/marathon --master local --zk zk://172.17.42.1:2181/mesos --http_port 8088
```
6. 运行Chronos
```bash
docker run -d -p 4400:8080 tomaskral/chronos --master zk://172.17.42.1:2181/mesos --zk_hosts zk://172.17.42.1:2181
```