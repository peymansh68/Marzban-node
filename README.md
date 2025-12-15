# Marzban-node

## manual installation
1. Install curl socat git and docker
```bash
apt install curl socat git -y && curl -fsSL https://get.docker.com | sh
```
2. clone marzban-node and run 
```bash
git clone https://github.com/peymansh68/Marzban-node && cd Marzban-node && docker compose up -d
```
if you want to install other xray version you should set RELEASE_TAG="latest" in intallxray.sh file 
for example 
just edit first line RELEASE_TAG="v25.10.15"

2. run 
```bash
docker compose up -d
```

if you want seperate outbound and routing from master you need to create a file name "custom-outbound.json" in /var/lib/marzban-node folder
if custom-outbound.json is not exist it uses outbounds and routing defined in Master
Tip: first routle of routing must be api
there is an example of outbound and routing you could find it



## More Info
Read the setup guide here: https://gozargah.github.io/marzban/docs/marzban-node
