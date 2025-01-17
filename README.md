# Dockerized Server
A N100 suite using only dockers that may communicate between each other.

This repo is my current mini server configuration. 
It works on Raspberry Pi OS 64 bits with minor changes but it is currently running on N100 CPu. With some slight changes of the mariadb containers, it can work on 32 bits, but I wouldn't recommand it will need old versions to be working.

I'm not a docker expert and I may have done some mistakes. So please, feel free to report any mistake or contact me in case of any remarks.

It provides the clean installation of:
 - A nginx proxy manager as a reverse proxy in order to manage the external accesses to your installation through the 443 port (https) through a nice interface.
   This container has to be launched first as it will also create the frontend network used by the other containers. 
 - Nextcloud for personnal files sharing and management
 - Photoprism which will handle your photo albums
 - A z2m folder which installs everything needed to use zigbee to mqtt as a broker for your zigbee installation :
   - Mosquitto
   - Zigbee2Mqtt
   - Home Assistant
  - A portainer container in order to have an interface to manage easily your containers. This part is in beta in my installation as containers were created before adding this container.
  - A transmission interface in order to easily download torrents on a local samba share while not at home.
  - A pyload instance in order to automate direct downloads

Please note that passwords have been changed to "CHANGE_ME" text but you will also need to change other things in configuration files (paths, smtp account, ...)
