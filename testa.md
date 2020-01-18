<a href="README.md"><< tillbaka</a>

# Test

## Testa mot Broker
```bash
// -h host, -t topic
mosquitto_sub -h broker-dns -t topic/subtopic

// -h host, -t topic, -m message
mosquitto_pub -h broker-dns -t topic/subtopic -m "testing testing..."
```
