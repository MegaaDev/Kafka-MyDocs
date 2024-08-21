# Kafka

Kafka with zookeeper is deprecated. Now there is a internal implementation (Kraft)

## Using docker

```bash
docker run -p 9092:9092 apache/kafka:3.7.1
```

## Get shell access to the container

```bash
docker ps
docker exec -it container_id /bin/bash
cd /opt/kafka/bin
```

## Create a topic

```bash
./kafka-topics.sh --create --topic quickstart-events --bootstrap-server localhost:9092
```

## Publish to the topic

```bash
./kafka-console-producer.sh --topic quickstart-events --bootstrap-server localhost:9092
```

## Consuming from the topic

```bash
./kafka-console-consumer.sh --topic quickstart-events --from-beginning --bootstrap-server localhost:9092
```
