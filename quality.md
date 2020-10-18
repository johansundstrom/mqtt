# MQTT Quality of Service

* Tre grader av tillförlitlighet mellan klienter och Broker
  * QoS 0 - fire and forget
  
    | MQTT klient | --publish--> | MQTT Broker |
    |---|---|---|
  
  * QoS 1 - meddelande lagras till PUBACK erhålls
    
    | MQTT klient | --publish --> | MQTT Broker |
    |---|---|---|
    | MQTT Klient | <-- PUBACK-- | MQTT Broker |
  
  * QoS 2 - Säkrast och långsammast
  
    | MQTT klient | --publish --> | MQTT Broker |
    |---|---|---|
    | MQTT Klient | <-- PUBACK-- | MQTT Broker |
    | MQTT Klient | -- PUBREL--> | MQTT Broker |
    | MQTT Klient | <--PUBCOMP-- | MQTT Broker |
