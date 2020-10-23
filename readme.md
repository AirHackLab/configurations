# Configuration
## Mosquitto
### Installation & Configuration de base
- sudo apt update && apt upgrade
- sudo apt install mosquitto
- cd /etc/mosquitto
- sudo mosquitto_passwd -c passwordfile VOTRE_PREMIER_UTILISATEUR
- sudo nano mosquitto.conf

Ajouter mosquitto.conf
```
allow_anonymous false
password_file /etc/mosquitto/passwordfile
```