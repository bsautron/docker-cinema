# docker-cinema
## Deluge
```sh
$ docker create --name=deluge --net=host -e PUID=1001 -e PGID=1001 -e TZ=Europe/Paris -v /home/cinema/deluge/downloads:/downloads -v /home/cinema/deluge/config:/config linuxserver/deluge
$ docker run -d --rm --tty --interactive -p 8112:8112 4e09138bfb18
```
