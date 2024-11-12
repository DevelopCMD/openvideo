# Discord Bot that edits videos and sometimes photos.
until the main one gets updated i would opt for this fork, removed some sketchy bits :)

## steps for smarterer people:
- install main reqs below
- clone with git/download repo to a folder (no spaces)
- open cmd in repo directory, install listed pip modules below with `pip install`
- restart cmd, run `discordBot.py` and all is good

## install requirements
- python 3.10-3.12
- ffmpeg 4.3+
- sox 14.4+
- config.json - configuration file, copy config.json.template to config.json and fill and edit to your own configuration
- cookies.txt (optional) - cookie file for downloads and whatnot

## pip requirements
- ffprobe-python
- ffmpeg-python
- discord.py
- pyjson5
- psutil
- Pillow==9.5.0
- yt-dlp
- pydub
- requests
