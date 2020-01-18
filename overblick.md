<a href="README.md"><< tillbaka</a>

# MQTT - Överblick

* Open Source
* IoT- eller Machine-to-machine (M2M) protokoll
* Klienter kommunicerar med servertjänsten - *Broker*
* Kommunikation sker via *Topics*
* Topics särskiljer logiskt 
* En klient kan vara *Publisher* eller *Subscriber*
* Sensorer sänder - Publisher
* Lampor lyssnar - Subscriber
* Broker har tre olika QoS
  - 0 levererar endast en gång (mest osäkert)
  - 1 levererar minst en gång (sänder och inväntar ACK)
  - 2 garanterad leverans en gång (långsamt men säkert)

## Installera Brokers
* Se <a href="installera.md">installera<a>

## Topics
* Användaren bestämmer namn på topics
* Topics kan bestå av flera undertopics - *Topic levels*
* Topic levels separeras med "/"
* Krav på ett Topic's namn
  * Case sensitive
  * UTF-8
  * Minst ett tecken
  * får inte vara <a href="https://github.com/mqtt/mqtt.github.io/wiki/SYS-Topics">$SYS</a> då detta är reserverat

## Subscribe av Multi- eller Single level topics

* Subscribe med Single level
```code
/
/b9
/b9/kitchen
/b9/kitchen/windowLights
/b9/kitchen/ceiling
/b9/office/ceiling
/b9/lounge
/b9/lounge/windowLights
/b9/lounge/lights
/b9/lounge/ceiling
```

* Subscribe med wildcard 
```/b9/lounge/#``` ger tre träffar
```code
/b9/lounge/ceiling
/b9/lounge/lights
/b9/lounge/windowLights
```

* Subscribe med wildcard
```/b9/+/ceiling``` ger tre träffar
```code
/b9/kitchen/ceiling
/b9/office/ceiling
/b9/lounge/ceiling
```

* Multilevel: Subscribe med multilevel wildcard
```/b9/+/#``` ger
```code
/b9/kitchen/windowLights
/b9/kitchen/ceiling
/b9/office/ceiling
/b9/lounge/windowLights
/b9/lounge/lights
/b9/lounge/ceiling
```
