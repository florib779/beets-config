This is a work, in a very early stage.

## Installation

`pip install https://github.com/beetbox/beets/tarball/master`

### Create a symlink

`sudo ln -s ~/.local/bin /usr/local/bin`

### Update

`pip install -U https://github.com/beetbox/beets/tarball/master`

## Goals

- [x] Submit acoustic analysis results to the AcousticBrainz server.
  * [absubmit](https://beets.readthedocs.io/en/latest/plugins/absubmit.html) (auto)
  * Install: `pip install requests`
- [x] Get acoustic-analysis information from the AcousticBrainz project.
  * [acousticbrainz](https://beets.readthedocs.io/en/latest/plugins/acousticbrainz.html) (auto)
- [x] Check for missing and corrupt files. 
  * [badfiles](https://beets.readthedocs.io/en/latest/plugins/badfiles.html) (manually)
    * Command: `beet bad`
- [x] Use bandcamp as an autotagger source, for fetching lyrics and cover art.
  * [bandcamp](https://github.com/unrblt/beets-bandcamp) (auto) @test
    * Install: `pip install beets-bandcamp`
- [x] Create folders with the first letters of the band names and assign them accordingly.
  * [bucket](https://beets.readthedocs.io/en/latest/plugins/bucket.html)
- [ ] Automatically checksum files to detect corruption.
  * [check](https://github.com/geigerzaehler/beets-check) (auto) @test
    * Install: `pip install beets-check`
- [x] Use acoustic fingerprinting to identify audio files with missing or incorrect metadata.
  * [chroma](https://beets.readthedocs.io/en/latest/plugins/chroma.html) (auto)
    * Install: `pip install pyacoustid`
- [x] Transcode Roon exports to redbook flac files for mobile devices.
  * [convert](https://beets.readthedocs.io/en/latest/plugins/convert.html)
    * Command: `beet convert`
- [x] Extend the autotagger’s search capabilities to include matches from the Discogs database.
  * [discogs](https://beets.readthedocs.io/en/latest/plugins/discogs.html) (auto)
    * Install: `pip install discogs-client`
- [ ] Find and list duplicate tracks or albums in the collection.
  * [duplicates](https://beets.readthedocs.io/en/latest/plugins/duplicates.html)
    * Command: `beet duplicates`
- [ ] Modify music metadata using your favorite text editor.
  * [edit](https://beets.readthedocs.io/en/latest/plugins/edit.html)
    * Command: `beet edit QUERY` # In case you need to edit the album-level fields, the recommended approach is to invoke the plugin via the command line in album mode after the import.
- [ ] Copy additional files (like covers, booklets) and directories during the import process. @test
  * [extrafiles](https://github.com/Holzhaus/beets-extrafiles)
    * Install: `pip install beets-extrafiles`
- [x] Fetch album art from different web sources.
  * [fetchart](https://beets.readthedocs.io/en/latest/plugins/fetchart.html) (auto)
    * Install: `pip install requests`
    - [ ] Fetch booklets - do not seem to be possible at the moment.
- [ ] Fetch artist covers and place them in the artist directories.
  * [fetchartist](https://github.com/dkanada/beets-fetchartist) (manually)
    * Install:
      * `pip install requests`
      * Copy to pluginpath
    * Command: beet fetchartist --help
    - [ ] `path not found`
- [x] Get notifications about new releases from album artists in your Beets library using muspy.
  * [follow](https://github.com/nolsto/beets-follow) (auto) @test
    * Install: `pip install beets-follow`
- [x] Tag albums that are missing tags altogether.
  * [fromfilename](https://beets.readthedocs.io/en/latest/plugins/fromfilename.html) (auto)
- [ ] Preserve the import date.
  * [importadded](https://beets.readthedocs.io/en/latest/plugins/importadded.html)
- [ ] Dump the current tag values for any file format supported by beets.
  * [info](https://beets.readthedocs.io/en/latest/plugins/info.html) (manually)
- [ ] Collect play counts from Last.fm. Doesn't make any sense for the use with Roon yet.
  * [lastimport](https://beets.readthedocs.io/en/latest/plugins/lastimport.html) (manually)
    * Install: `pip install pylast`
    * Command: `beet -v lastimport`
    * To keep up-to-date, you can run this plugin every once in a while (cron?).
- [x] Fetch genres from Last.fm. MusicBrainz actually doesn’t contain genre information and set a fallback genre if none is available.
  * [lastgenre](https://beets.readthedocs.io/en/latest/plugins/lastgenre.html)
    * Install: `pip install pylast`
- [x] Fetch lyrics from various sources.
  * [lyrics](https://beets.readthedocs.io/en/latest/plugins/lyrics.html)
    * Install: `pip install requests`
- [x] Submit the catalog to MusicBrainz to maintain the music collection list there. (auto)
  * [mbcollection](https://beets.readthedocs.io/en/latest/plugins/mbcollection.html)
  - [ ] Remove (manually): `beet mbupdate -r`
- [x] Fetch metadata from MusicBrainz for albums and tracks that already have MusicBrainz IDs.
  * [mbsync](https://beets.readthedocs.io/en/latest/plugins/mbsync.html)
- [ ] Find and list, which or how many tracks are missing, for every album in the collection.
  * [missing](https://beets.readthedocs.io/en/latest/plugins/missing.html)
- [ ] Set file permissions for imported music files and its directories.
  * [permissions](https://beets.readthedocs.io/en/latest/plugins/permissions.html) (auto)
- [ ] Fetch oldest recording or release date for each track.
  * [oldestdate](https://github.com/kernitus/beets-oldestdate)
    * Copy to pluginpath
- [x] Add ReplayGain tags for mobile devices.
  * [replaygain](https://beets.readthedocs.io/en/latest/plugins/replaygain.html)
- [ ] Remove extraneous metadata from files’ tags.
  * [scrub](https://beets.readthedocs.io/en/latest/plugins/scrub.html)
- [ ] Add own tags, like `ROONALBUMTAG`, `ROONTRACKTAG` ...
  - [ ] Write track genres to `ROONTRAGTAG`
  - [ ] Automatically add `ROONRADIOBAN`, value `false`, if the tag doesn't exist.
  * [usertag](https://github.com/igordertigor/beets-usertag)
    * Install: `pip install git+git://github.com/igordertigor/beets-usertag.git`
- [x] List all files in the library folder which are not listed in the beets library database.
  * [unimported](https://beets.readthedocs.io/en/latest/plugins/unimported.html)
- [x] Web interface.
  * [web](https://beets.readthedocs.io/en/latest/plugins/web.html)
    * Install: `pip install flask`
- [ ] Null fields in files’ metadata tags.
  * [zero](https://beets.readthedocs.io/en/latest/plugins/zero.html)
- [ ] Fetch `website` tag.
- [ ] Fetch `barcode` tag.
- [ ] Fetch `isrc` tag.
- [ ] Fetch `origninalyear` tag.
- [ ] Fetch `artists` tag.
- [x] Automatically extract compressed archives in Download directory.
  * Only seem to work for single files, for example: `beet import ~/beets-music/Album.zip`
  * Doesn't work with whitespaces in file names.
- [ ] Assign Qobuz comment/description to the appropriate tags.
  * https://discourse.beets.io/t/comments-field-template-dev-questions/1354
- [ ] Refine matches.
- [x] Hide credentials in `config.yaml` (`secrets.yaml`).

## Beets commands

Of course, the given commands assume that the music files to import are located in `~/Downloads/`, otherwise the path must be changed.

`beet import ~/Downloads/` # Import and change tags.

`beet import -A ~/Downloads/` # Import but don't change any tags.

`beet import -W ~/Downloads/` # When autotagging, don’t write new tags to the files themselves (just keep the new metadata in beets’ database.)

`beet import -C ~/Downloads/` # Don’t copy imported files to your music directory; leave them where they are.

`beet import -m ~/Downloads/` # Move imported files to your music directory (overrides the -c option).

`beet import -l LOGFILE ~/Downloads/` # Write a message to `LOGFILE` every time you skip an album or choose to take its tags “as-is” (see below) or the album is skipped as a duplicate; this lets you come back later and reexamine albums that weren’t tagged successfully.

`beet import -q ~/Downloads/` # Quiet mode. Never prompt for input and, instead, conservatively skip any albums that need your opinion. The `-ql` combination is recommended.

`beet import -t ~/Downloads/` # Timid mode, which is sort of the opposite of “quiet.” The importer will ask your permission for everything it does, confirming even very good matches with a prompt.

`beet import -p ~/Downloads/` # Automatically resume an interrupted import. The importer keeps track of imports that don’t finish completely (either due to a crash or because you stop them halfway through) and, by default, prompts you to decide whether to resume them. The `-p` flag automatically says “yes” to this question. Relatedly, `-P` flag automatically says “no.”

`beet import -s ~/Downloads/` # Run in singleton mode, tagging individual tracks instead of whole albums at a time. See the “as Tracks” choice below. This means you can use beet import `-AC` to quickly add a bunch of files to your library without doing anything to them.

`beet import -g ~/Downloads/` # Assume there are multiple albums contained in each directory. The tracks contained a directory are grouped by album artist and album name and you will be asked to import each of these groups separately. See the “Group albums” choice below.



`beet update`

`beet stats`

`beet ls` # List all music of the library

`beet ls -a` # List all albums of the library

`beet rm <part of name>` # Remove track(s) of the library

`beet rm -a <part of name>` # Remove album(s) of the library

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
