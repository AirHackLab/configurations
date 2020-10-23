# Configuration
## Mosquitto
### Installation & Configuration de base
https://iooner.io/installer-un-broker-mqtt-mosquitto-ubuntu/
```
sudo apt update && apt upgrade
sudo apt install mosquitto
cd /etc/mosquitto
sudo mosquitto_passwd -c passwordfile VOTRE_PREMIER_UTILISATEUR
sudo nano mosquitto.conf
```

Ajouter mosquitto.conf
```
allow_anonymous false
password_file /etc/mosquitto/passwordfile
```


## Influx
https://docs.influxdata.com/influxdb/v1.8/introduction/install/
```
wget -qO- https://repos.influxdata.com/influxdb.key | sudo apt-key add -
source /etc/lsb-release
echo "deb https://repos.influxdata.com/${DISTRIB_ID,,} ${DISTRIB_CODENAME} stable" | tee /etc/apt/sources.list.d/influxdb.list
apt update
apt install influxdb
service influxdb start
```