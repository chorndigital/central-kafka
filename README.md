# Central Kafka

## Testing

## 1. Using Kafka CLI (inside container)

**Produce a message**

```
docker exec -it kafka kafka-console-producer \
  --broker-list kafka:9092 \
  --topic test-topic
```

Then type some message

```
hello world
order-123
```

**Consume messages**
Open another terminal and run:

```
docker exec -it kafka kafka-console-consumer \
  --bootstrap-server kafka:9092 \
  --topic test-topic \
  --from-beginning
```

Expect seeing:

```
hello world
order-123
```