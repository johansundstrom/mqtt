<a href="README.md"><< tillbaka</a>

# Installera

## Installera på Raspberry Pi
http://www.switchdoc.com/2016/02/tutorial-installing-and-testing-mosquitto-mqtt-on-raspberry-pi/

(Testad och verifierad)

## Installera på LINUX
```bash
sudo apt-get install mosquito mosquito-clients
```

(Testad och verifierad)

## Installera på Windows
https://www.eclipse.org/mosquitto/download
välj mosquitto-1.4.15-install-win32.exe då den kompenserar för fler beroenden.
Observera att båda versionerna har beroenden och att flera DLL's behöver installeras utöver installationspaketet. Mer info i readme-windows.txt.

(saknas ssleay32.dll och libeay32.dll)

## Installera på MAC
http://macappstore.org/mosquitto/

(ej testad)

## Installera på Arduino
Flera bibliotek finns. Jag rekommenderar PubSubClient av Nick O'Leary.

## Testa Broker
```bash
// Starta subscriber. -h host, -t topic
mosquitto_sub -h localhost -t test

// Starta publisher. -m message
mosquitto_pub -h localhost -t test -m "testing testing..."
```
