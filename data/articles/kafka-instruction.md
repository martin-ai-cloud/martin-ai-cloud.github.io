# QuickStart

## docker部署
```bash
docker run -p 9092:9092 apache/kafka:4.1.1
```

## 操作
### 显示topics列表
```bash
./kafka-topics.sh --list --bootstrap-server localhost:9092
```

### 新建topic
```bash
./kafka-topics.sh --bootstrap-server localhost:9092 --create --topic test-topic
```

### 生产event
```bash
./kafka-console-producer.sh --bootstrap-server localhost:9092 --topic test-topic
```

### 消费event
```bash
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test-topic --from-beginning
```