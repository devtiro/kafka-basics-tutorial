# Kafka Basics Tutorial

### Create Topic
```
docker exec broker \
kafka-topics --bootstrap-server broker:9092 \
             --create \
             --topic "devtiro"
```

### Kafka Producer
```
docker exec --interactive --tty broker \
   kafka-console-producer --bootstrap-server broker:9092 \
                          --topic "devtiro"
```

### Kafka Consumer
```
docker exec --interactive --tty broker \
kafka-console-consumer --bootstrap-server broker:9092 \
                       --topic "devtiro" \
                       --from-beginning
```
