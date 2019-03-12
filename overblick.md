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
/b9/1/sovrum
/b9/2/rum/kök
/b9/2/rum/vardagsrum
/b9/2/rum/hall
```

* Subscribe med wildcard - /b9/2/#
```code
/b9/2/rum/kök
/b9/2/rum/vardagsrum
/b9/2/rum/hall
```

* Subscribe med wildcard - /b9/+/+/strömbrytare
```code
/b9/1/sovrum/strömbrytare
/b9/2/kök/strömbrytare
/b9/2/vardagsrum/strömbrytare
```

* Multilevel: Subscribe av /b9/2/# -- tre träffar
