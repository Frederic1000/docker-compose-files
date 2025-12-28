# docker-compose.yaml files
Docker compose files  
I'm using a big docker-compose file with a stack of all my containers.

Remote access is done via Tailscale, I'm using tsdproxy to create the tailscale machine for each container.  
Tailscale is also running natively (ie not via docker) in my host machine.

Services:
- Tailscale via tsdproxy: VPN and HTTPS access to all the containers
- Wireguard: VPN access to the host machine and to the local network
- Home Assistant: Home automation
- Mosquitto: IOT with Home Assistant
- Duplicati: Backup of Home Assistant configuration files
- AdGuard: ad blocking software, over Tailscale= also active out of home. It will block ads to all machines connected to the Tailscale network (pc, mac, phones,...)
- Stirling pdf: pdf edition
- Node-red (uncomment to use): home automation
- NightScout-LibreLink-Up (uncomment to use): Upload LibreLink data to NightScout database

Environment variables are in the .env file, this is where secrets are stored (URL, password, email, username,...)
