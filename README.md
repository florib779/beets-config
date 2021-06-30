## Installation

### Docker

* https://hub.docker.com/r/linuxserver/beets
* https://github.com/justifiably/docker-beets (inspiration)

#### Systemd

`nano /etc/systemd/system/beets-docker.service´

`
docker run -d \
  --name=beets \
  -e PUID=1000 \ # flori
  -e PGID=1000 \ # flori
  -e TZ=Europe/Berlin \
  -p 8337:8337 \
  -v /home/flori/.config/beets:/config \
  -v /home/flori/beets-music:/music \
  -v /home/flori/Downloads:/downloads \
  --restart unless-stopped \
  ghcr.io/linuxserver/beets
`

`systemctl start beets-docker`

`systemctl enable beets-docker`

#### Commands

##### Command prompt as user flori

`docker exec -it -u flori beets bash`

##### Shell access whilst the container is running

`docker exec -it beets /bin/bash`

##### Monitor the logs of the container in realtime

`docker logs -f beets`

##### Container version number

`docker inspect -f '{{ index .Config.Labels "build_version" }}' beets`


##### Image version number

`docker inspect -f '{{ index .Config.Labels "build_version" }}' ghcr.io/linuxserver/beets`

##### Update the image

`docker pull ghcr.io/linuxserver/beets`


## Installed Plugins

## Not installed Plugins, but already in config.yaml

## ToDo/Ideas

## Commands

Of course, the given commands assume that the music files are located in `~/beets-music/`, otherwise the path must be changed.

### Import and change tags

`beet import ~/beets-music/`

### Import but don't change any tags

`beet import -A ~/beets-music/`

### Add the single track without an album

`beet import -s ~/beets-music/`

### Fetch lyrics for the entiry library

`beet lyrics`

### Stats

`beet stats`

### List all music of the library

`beet list` or `beet ls`

### List all albums of the library

`beet ls -a`

### Remove track(s) of the library

`beet rm <part of name>`

### Remove album(s) of the library

`beet rm -a <part of name>`

## Tips

### Enabling tab-completion in bash

Beets includes support for Bash shell command completion. To enable completion, put the following line into your `.bashrc`:

```
~/.bashrc

eval "$(beet completion)"
```

You will also need to install `bash-completion` for this to work. 

## Links

* [Beets @ Linux-Community (German)](https://www.linux-community.de/ausgaben/linuxuser/2011/02/musiksammlungen-verwalten-mit-beets/)
* [Beets @ hafenfragen.de (German)](https://www.hagenfragen.de/linux-tipps/software/mp3-musiksammlung-organisieren-mit-beets.html)
* [Beets @ jundar.de (German)](https://jundar.de/beets-konfigurieren/)
* [Beets Docker](https://blog.linuxserver.io/2016/10/08/managing-your-music-collection-with-beets/)
