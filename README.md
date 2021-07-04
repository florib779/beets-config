## Plugins

I have a [Manjaro Linux](https://manjaro.org/) based installation therefore, a different installation method must be used for other distributions, or the names of the installation files may differ.

### Installed

* [absubmit](https://beets.readthedocs.io/en/stable/plugins/absubmit.html) (auto)
  * Install: `pacman -S acousticbrainz-client`
* [acousticbrainz](https://beets.readthedocs.io/en/stable/plugins/acousticbrainz.html) (auto)
* [badfiles](https://beets.readthedocs.io/en/stable/plugins/badfiles.html) (auto)
  * Command: `beet -c ~/.config/beets/secrets.yaml bad`
* [bandcamp](https://github.com/unrblt/beets-bandcamp) (auto)
  * Install: `beets-bandcamp` (AUR)
* [bucket](https://beets.readthedocs.io/en/stable/plugins/bucket.html)
* [check](https://github.com/geigerzaehler/beets-check)
  * Install: `beets-check` (AUR)
* [chroma](https://beets.readthedocs.io/en/stable/plugins/chroma.html) (auto)
  * Install: `pacman -S python-pyacousticid` (seems to work without installing this library) @test
* [discogs](https://beets.readthedocs.io/en/stable/plugins/discogs.html) (auto)
  * Install: `pacman -S python-discogs-client`
* [duplicates](https://beets.readthedocs.io/en/stable/plugins/duplicates.html)
  * Command: `beet duplicates`
* [edit](https://beets.readthedocs.io/en/stable/plugins/edit.html)
  * Command: `beet -c ~/.config/beets/secrets.yaml edit QUERY`
* [extrafiles](https://github.com/Holzhaus/beets-extrafiles)
  * Install: `beets-extrafiles` (AUR)
* [fetchart](https://beets.readthedocs.io/en/stable/plugins/fetchart.html) (auto)
* [fromfilename](https://beets.readthedocs.io/en/stable/plugins/fromfilename.html) (auto)
* [importadded](https://beets.readthedocs.io/en/stable/plugins/importadded.html)
* [lastimport](https://beets.readthedocs.io/en/stable/plugins/lastimport.html)
  * Install: `pacman -S python-pylast`
  * Command: `beet -c ~/.config/beets/secrets.yaml -c ~/.config/beets/secrets.yaml -v lastimport`
  * To keep up-to-date, you can run this plugin every once in a while (cron?).

### Not installed/configured, but already in config.yaml

* [convert](https://beets.readthedocs.io/en/stable/plugins/convert.html)
* [follow](https://github.com/nolsto/beets-follow)
  * Install `pacman -S beets-follow-git`
  * ToDo: Error message
* [fetchartist](https://github.com/dkanada/beets-fetchartist)
* [ftintitle](https://beets.readthedocs.io/en/stable/plugins/ftintitle.html)
* [oldestdate](https://github.com/kernitus/beets-oldestdate)
## ToDo/Ideas

- [x] Hide credentials in `config.yaml` (secrets)
  * Command: `beet -c ~/.config/beets/secrets.yaml ...`
- [ ] Fetch Booklets
- [ ] Fetch `website`
- [ ] Fetch `barcode`
- [ ] Fetch `isrc`
- [ ] Fetch `origninalyear`
- [ ] Fetch `artists`

## Beets commands

Of course, the given commands assume that the music files are located in `~/beets-music/`, otherwise the path must be changed.

`beet -c ~/.config/beets/secrets.yaml import ~/Downloads/ # Import and change tags`

`beet -c ~/.config/beets/secrets.yaml import -A ~/Downloads/ # Import but don't change any tags`

`beet -c ~/.config/beets/secrets.yaml import -s ~/Downloads/ # Add the single track without an album`

`beet -c ~/.config/beets/secrets.yaml update`

`beet -c ~/.config/beets/secrets.yaml stats`

`beet -c ~/.config/beets/secrets.yaml ls # List all music of the library`

`beet -c ~/.config/beets/secrets.yaml ls -a # List all albums of the library`

`beet -c ~/.config/beets/secrets.yaml rm <part of name> # Remove track(s) of the library`

`beet -c ~/.config/beets/secrets.yaml rm -a <part of name> # Remove album(s) of the library`

## Tips

### Enabling tab-completion in bash

Beets includes support for Bash shell command completion. To enable completion, put the following line into your `.bashrc`:

```
~/.bashrc

eval "$(beet completion)"
```

You will also need to install `bash-completion` for this to work. 

## Links

* [Documentation](https://beets.readthedocs.io)
* [Beets @ Linux-Community (German)](https://www.linux-community.de/ausgaben/linuxuser/2011/02/musiksammlungen-verwalten-mit-beets/)
* [Beets @ hafenfragen.de (German)](https://www.hagenfragen.de/linux-tipps/software/mp3-musiksammlung-organisieren-mit-beets.html)
* [Beets @ jundar.de (German)](https://jundar.de/beets-konfigurieren/)
* [Beets Docker](https://blog.linuxserver.io/2016/10/08/managing-your-music-collection-with-beets/)

### Configs

* https://github.com/hashhar/picard-beets-config
* https://github.com/kergoth/Beets-Library
* https://github.com/RollingStar/dial-beets
