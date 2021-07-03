## Plugins

I have a [Manjaro Linux](https://manjaro.org/) based installation therefore, a different installation method must be used for other distributions, or the names of the installation files may differ.

### Installed

* [absubmit](https://beets.readthedocs.io/en/stable/plugins/absubmit.html) (auto)
  * `acousticbrainz-client`
* [acousticbrainz](https://beets.readthedocs.io/en/stable/plugins/acousticbrainz.html) (auto)
* [badfiles](https://beets.readthedocs.io/en/stable/plugins/badfiles.html) (auto)
  * Command: `beet bad`
* [chroma](https://beets.readthedocs.io/en/stable/plugins/chroma.html) (auto)
  * Install `python-pyacousticid` (seems to work without installing this library) @test
* [discogs](https://beets.readthedocs.io/en/stable/plugins/discogs.html) (auto)
  * Install `python-discogs-client`
* [duplicates](https://beets.readthedocs.io/en/stable/plugins/duplicates.html)
  * Command: `beet duplicates`
* [edit](https://beets.readthedocs.io/en/stable/plugins/edit.html)
  * Command: `beet edit QUERY`
* [fetchart](https://beets.readthedocs.io/en/stable/plugins/fetchart.html) (auto)

### Not installed, but already in config.yaml

* [artiscountry](https://github.com/agrausem/beets-artistcountry)
* [bandcamp](https://github.com/unrblt/beets-bandcamp)
  * Install `beets-bandcamp` (AUR)
* [bucket](https://beets.readthedocs.io/en/stable/plugins/bucket.html)
* [check](https://github.com/geigerzaehler/beets-check)
* [convert](https://beets.readthedocs.io/en/stable/plugins/convert.html)
* [copyartifacts](https://github.com/sbarakat/beets-copyartifacts) (no longer maintained, but alternatives available)
* [follow](https://github.com/nolsto/beets-follow)
* [fromfilename](https://beets.readthedocs.io/en/stable/plugins/fromfilename.html) (auto)

## ToDo/Ideas

- [ ] Hide credentials (secrets)
- [ ] Fetch Booklets

## Beets commands

Of course, the given commands assume that the music files are located in `~/beets-music/`, otherwise the path must be changed.

`beet import ~/Downloads/ # Import and change tags`

`beet import -A ~/Downloads/ # Import but don't change any tags`

`beet import -s ~/Downloads/ # Add the single track without an album`

`beet stats`

`beet ls # List all music of the library`

`beet ls -a # List all albums of the library`

`beet rm <part of name> # Remove track(s) of the library`

`beet rm -a <part of name> # Remove album(s) of the library`

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
