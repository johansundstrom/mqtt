<a href="README.md"><< tillbaka</a>

# Installera

## Installera på Raspberry Pi
http://www.switchdoc.com/2016/02/tutorial-installing-and-testing-mosquitto-mqtt-on-raspberry-pi/

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt install -y mosquitto mosquitto-clients
```

(Testad och verifierad)

## Installera på LINUX
```bash
sudo apt-get install mosquitto mosquitto-clients
```

(Testad och verifierad)

## Installera på Windows
https://www.eclipse.org/mosquitto/download
välj mosquitto-1.4.15-install-win32.exe då den kompenserar för fler beroenden.
Observera att båda versionerna har beroenden och att flera DLL's behöver installeras utöver installationspaketet. Mer info i readme-windows.txt.

(Testad och verifierad)

## Installera på MAC
http://macappstore.org/mosquitto/

(Testad och verifierad)

## Installera på Arduino
Flera bibliotek finns. Jag rekommenderar PubSubClient av Nick O'Leary.

(Testad och verifierad)

## Installera MQTT-Explorer (GUI-verktyg)
http://mqtt-explorer.com/
Fungerar mot alla plattformar (Windows/Mac/Ubuntu/Linux)

