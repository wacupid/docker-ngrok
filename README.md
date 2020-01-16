# DOCKER NGROK IMAGE

## BUILD IMAGE

```linux
git clone https://github.com/wacupid/docker-ngrok.git
cd docker-ngrok
docker build -t wacupid/ngrok .
```

## RUN
* you must mount your folder (E.g `/data/ngrok`) to container `/myfiles`
* if it is the first run, it will generate the binaries file and CA in your floder `/data/ngrok`

```linux
docker run -idt --name ngrok-server \
-v /data/ngrok:/myfiles \
-e DOMAIN='wacupid.tk' wacupid/ngrok /bin/sh /server.sh
```
