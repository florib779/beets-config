## Installed Plugins

## Not installed Plugins, but already in config.yaml

## ToDo/Ideas

- [ ] Hide credentials (secrets)

## Beets commands

Of course, the given commands assume that the music files are located in `~/beets-music/`, otherwise the path must be changed.

### Import and change tags

`beet import ~/Downloads/`

### Import but don't change any tags

`beet import -A ~/Downloads/`

### Add the single track without an album

`beet import -s ~/Downloads/`

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
