<a href="README.md"><< tillbaka</a>

# Test av Eclipse Mosquitto

Starta en terminal

## Skapa en Subscriber

-h host, -t topic, -m message

```bash
mosquitto_sub -h broker-dns -t topic/subtopic
```

## Skapa en Publisher

```bash
mosquitto_pub -h broker-dns -t topic/subtopic -m "testing testing..."
```
