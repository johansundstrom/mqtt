# MQTT
Summariskt om MQTT

## Installera på Raspberry Pi
http://www.switchdoc.com/2016/02/tutorial-installing-and-testing-mosquitto-mqtt-on-raspberry-pi/

## Installera på LINUX
```bash
sudo apt-get install mosquito mosquito-clients
```

## Installera på Windows 


## Testa Broker
```bash
// Starta subscriber. -h host, -t topic
mosquitto_sub -h localhost -t test

// Starta publisher. -m message
mosquitto_pub -h localhost -t test -m "hello world"
```
