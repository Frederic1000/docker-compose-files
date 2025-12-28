# docker-compose.yaml files
Docker compose files  
I'm using a big docker-compose file with a stack of all my containers.

Remote access is done via Tailscale, I'm using tsdproxy to create the tailscale machine for each container.  
Tailscale is also running natively (ie not via docker) in my host machine.
