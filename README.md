# Marzban-node current xray version is v25.10.15

## manual installation
1. Install curl socat git and docker
```bash
apt install curl socat git -y && curl -fsSL https://get.docker.com | sh
```
2. clone marzban-node and run 
```bash
git clone https://github.com/peymansh68/Marzban-node && cd Marzban-node
```
if you want to install other xray version you should set RELEASE_TAG="latest" in intallxray.sh file 
.
just edit first line RELEASE_TAG="v25.10.15"

3. run 
```bash
docker compose up -d
```

if you want seperate outbound and routing from master you need to create a file name "custom-outbound.json" in /var/lib/marzban-node folder
if custom-outbound.json is not exist it uses outbounds and routing defined in Master
Tip: first roule of routing must be api
there is an example of outbound and routing you could find it

how to remove image and recreate the project? it is usefull "when you want to change xray version"
step 1:
```bash
docker compose down --remove-orphans --rmi all
```
step 2:
now you can run docker compose up -d it will create the new image
```bash
docker compose up -d
```



## More Info
Read the setup guide here: https://gozargah.github.io/marzban/docs/marzban-node
