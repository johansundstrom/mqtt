# MQTT Quality of Service

* Tre grader av tillförlitlighet mellan klienter och Broker
  * QoS 0 - fire and forget
  
  MQTT klient --publish--> MQTT Broker
  
  * QoS 1 - meddelande lagras till PUBACK erhålls
  * QoS 2 - Säkrast och långsammast
