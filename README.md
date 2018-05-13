## Deluge
```sh
$ docker create \
--name=deluge \
--net=host \
-e PUID=1001 \
-e PGID=1001 \
-e TZ="Europe/Paris" \
-v /home/cinema/deluge/downloads:/downloads \
-v /home/cinema/deluge/config:/config \
linuxserver/deluge
```
```sh
$ docker run -d --rm --tty --interactive -p 8112:8112 linuxserver/deluge
```

## Transmission
```sh
$ docker create --name=transmission \
-v /home/cinema/transmission/config:/config \
-v /home/cinema/transmission/downloads:/downloads \
-v /home/cinema/transmission/watch:/watch \
-e PGID=1001 -e PUID=1001 \
-e TZ="Europe/Paris" \
-p 9091:9091 -p 51413:51413 \
-p 51413:51413/udp \
linuxserver/transmission
```
```sh
$ docker run --rm -i --tty linuxserver/transmission
```
