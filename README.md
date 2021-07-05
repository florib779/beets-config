This is a work, in a very early stage.

I have a [Manjaro Linux](https://manjaro.org/) based installation therefore, a different installation method must be used for other distributions, or the names of the installation files may differ.

### Goals

- [x] Submit acoustic analysis results to the AcousticBrainz server.
  * [absubmit](https://beets.readthedocs.io/en/stable/plugins/absubmit.html) (auto)
    * Install: `pacman -S acousticbrainz-client`
- [x] Get acoustic-analysis information from the AcousticBrainz project.
  * [acousticbrainz](https://beets.readthedocs.io/en/stable/plugins/acousticbrainz.html) (auto)
- [x] Check for missing and corrupt files. 
  * [badfiles](https://beets.readthedocs.io/en/stable/plugins/badfiles.html) (manually)
    * Command: `beet -c ~/.config/beets/secrets.yaml bad`
- [ ] Use bandcamp as an autotagger source, for fetching lyrics and cover art.
  * [bandcamp](https://github.com/unrblt/beets-bandcamp) (auto) @test
    * Install: `beets-bandcamp` (AUR)
- [x] Create folders with the first letters of the band names and assign them accordingly.
  * [bucket](https://beets.readthedocs.io/en/stable/plugins/bucket.html)
- [ ] Automatically checksum files to detect corruption.
  * [check](https://github.com/geigerzaehler/beets-check) (auto) @test
    * Install: `beets-check` (AUR)
- [x] Use acoustic fingerprinting to identify audio files with missing or incorrect metadata.
  * [chroma](https://beets.readthedocs.io/en/stable/plugins/chroma.html) (auto)
    * Install: `pacman -S python-pyacousticid` (seems to work without installing this library) @test
- [ ] Convert parts of the collection to a directory of your choice, transcoding audio (and embedding album art - this is done by the Roon export function) along the way for mobile devices.
  * [convert](https://beets.readthedocs.io/en/stable/plugins/convert.html)
- [x] Extend the autotagger’s search capabilities to include matches from the Discogs database.
  * [discogs](https://beets.readthedocs.io/en/stable/plugins/discogs.html) (auto)
    * Install: `pacman -S python-discogs-client`
- [ ] Find and list duplicate tracks or albums in the collection.
  * [duplicates](https://beets.readthedocs.io/en/stable/plugins/duplicates.html)
    * Command: `beet duplicates`
- [ ] Modify music metadata using your favorite text editor.
  * [edit](https://beets.readthedocs.io/en/stable/plugins/edit.html)
    * Command: `beet -c ~/.config/beets/secrets.yaml edit QUERY`
- [ ] Copy additional files (like covers, booklets) and directories during the import process. @test
  * [extrafiles](https://github.com/Holzhaus/beets-extrafiles)
    * Install: `beets-extrafiles` (AUR)
- [x] Fetch album art from different web sources.
  * [fetchart](https://beets.readthedocs.io/en/stable/plugins/fetchart.html) (auto)
  * Booklets do not seem to be possible at the moment.
- [ ] Fetch artist covers and place them in the artist directories.
  * [fetchartist](https://github.com/dkanada/beets-fetchartist)
    * Install: `pacman -S python-pylast`
- [ ] Get notifications about new releases from album artists in your Beets library using muspy.
  * [follow](https://github.com/nolsto/beets-follow) (auto) @test
    * Install: `pacman -S beets-follow-git`
    * Command: `beet -c ~/.config/beets/secrets.yaml follow`
- [x] Tag albums that are missing tags altogether.
  * [fromfilename](https://beets.readthedocs.io/en/stable/plugins/fromfilename.html) (auto)
- [ ] Preserve the import date.
  * [importadded](https://beets.readthedocs.io/en/stable/plugins/importadded.html)
- [ ] Dump the current tag values for any file format supported by beets.
  * [info](https://beets.readthedocs.io/en/stable/plugins/info.html)
- [ ] Collect play counts from Last.fm. Doesn't make any sense for the use with Roon yet.
  * [lastimport](https://beets.readthedocs.io/en/stable/plugins/lastimport.html) (manually)
    * Install: `pacman -S python-pylast`
    * Command: `beet -c ~/.config/beets/secrets.yaml -v lastimport`
    * To keep up-to-date, you can run this plugin every once in a while (cron?).
- [ ] Fetch genres from Last.fm. MusicBrainz actually doesn’t contain genre information.
  * [lastgenre](https://beets.readthedocs.io/en/stable/plugins/lastgenre.html)
- [x] Fetch lyrics from various sources.
  * [lyrics](https://beets.readthedocs.io/en/stable/plugins/lyrics.html)
- [x] Submit the catalog to MusicBrainz to maintain the music collection list there.
  * [mbcollection](https://beets.readthedocs.io/en/stable/plugins/mbcollection.html)
- [ ] Fetch metadata from MusicBrainz for albums and tracks that already have MusicBrainz IDs.
  * [mbsync](https://beets.readthedocs.io/en/stable/plugins/mbsync.html)
- [ ] Find and list, which or how many tracks are missing, for every album in the collection.
  * [missing](https://beets.readthedocs.io/en/stable/plugins/missing.html)
- [ ] Set file permissions for imported music files and its directories.
  * [permissions](https://beets.readthedocs.io/en/stable/plugins/permissions.html)
- [ ] Fetch oldest recording or release date for each track.
  * [oldestdate](https://github.com/kernitus/beets-oldestdate)
  - [ ] Add ReplayGain tags for mobile devices.
    * [replaygain](https://beets.readthedocs.io/en/stable/plugins/replaygain.html)
- [ ] Remove extraneous metadata from files’ tags.
  * [scrub](https://beets.readthedocs.io/en/stable/plugins/scrub.html)
- [ ] Add own tags, like `ROONALBUMTAG`, `ROONTRACKTAG` ...
  * [usertag](https://github.com/igordertigor/beets-usertag)
- [x] Web interface.
  * [web](https://beets.readthedocs.io/en/stable/plugins/web.html)
- [ ] Fetch genres from various music sites.
  * wlg (whatlastgenre)
    * ToDo: What is the difference to "lastgenre"?
- [ ] Null fields in files’ metadata tags.
  * [zero](https://beets.readthedocs.io/en/stable/plugins/zero.html)
- [ ] Fetch Booklets
- [ ] Fetch `website` tag
- [ ] Fetch `barcode` tag
- [ ] Fetch `isrc` tag
- [ ] Fetch `origninalyear` tag
- [ ] Fetch `artists` tag
- [ ] Automatically extract archives
- [x] Hide credentials in `config.yaml` (secrets)
  * Command: `beet -c ~/.config/beets/secrets.yaml ...`

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
* [Beets @ jundar.de (German)](https://jundar.de/beets-konfigurieren/)
* [Beets Docker](https://blog.linuxserver.io/2016/10/08/managing-your-music-collection-with-beets/)

### Configs

* https://github.com/hashhar/picard-beets-config
* https://github.com/kergoth/Beets-Library
* https://github.com/RollingStar/dial-beets
