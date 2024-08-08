# Commands Documentation

## Editing commands

### Destroy command:
The `destroy [<arg1>=<val1>,<arg2>=<val2>,...]` commands edits a video according to the parameters </br>
- `destroy bass=100` or `destroy bass 100`

To use multiple commands, use `,` to separate them
- `bass=100, hypercam`

To use multiple groups of commands, use `|` to separate groups of commands.
- `ytp=100,toptext=hi|hcycle=3`

### Download command:  
The `download <video>` command takes one parameter `video` as a search query and downloads the first result regardless of URL (no idea why)
- `download funny video` or `download <URL/video ID>`
- Not always reliable, up to 8 MB (?)

### Concat command:  
The `concat <n> [<video1>, <video2>, ...]` command can take in `<n>` videos and concatinate them. You can type just the start of the filename to order them.
- `concat 2 g h`
- Say the channel has two recent videos "hello.mp4" and "goodbye.mp4", this concatinates the videos with "goodbye.mp4" coming first

## Metacommands:

### Pecking order:

When doing an editing command, the order is as followed:
- Attachments > attachments of replied to message > recent messages in channel
    
### Command chaining:
You can link together commands using `>>` between them.
- `download funny video >> destroy speed 5, toptext hello` would download `funny video`, post it, then add a caption "hello"
- Often comes with cooldown though and sometimes unreliable
    
By adding `!` at the start of a command, the bot, when replying to itself, will override the previous message by deleting it before sending the result.
- `!download woman dancing >> !destroy e 30, speed 5, mute, music penis music, musicskip 8 >> download man dancing >> !destroy e 30, speed 5, mute, music dramatic music, musicskip 25, volume 2 >> concat >> cap face off`
- This will download two videos, speed up, mute, add a song and caption to them, and then finally concatinate them

# Command List
### Video and Audio commands:
| Command         | Shorthand   | Type   | Min  | Max          | Description                                                                                         |
|-----------------|-------------|--------|------|--------------|-----------------------------------------------------------------------------------------------------|
| `delfirst`      | `delf`      | -      | -    | -            | When selection is enabled, deletes parts of video before `start`                                    |
| `dellast`       | `dell`      | -      | -    | -            | When selection is enabled, deletes parts of video after `end`                                       |
| `end`           | `e`         | Number | 0    | End of video | Time when video ends, in seconds. (Or end of effect with `selection`)                               |
| `playreverse`   | `prev`      | Number | 1    | 2            | 1 = plays, then reverses. 2 = reverses, then plays the video                                        |
| `repeatuntil`   | `repu`      | Number | 1    | 45           | Repeats video until this time is reached                                                            |
| `reverse`       | `rev`       | -      | -    | -            | Reverses the video and audio                                                                        |
| `ricecake`      | `rc`        | Number | 1    | 100          | Clones delta frames (corrupting video) and clones audio                                             |
| `rlag`          | `rlag`      | Number | 1    | 100          | Shuffles frames in chunks.                                                                          |
| `selection`     | `se`        | -      | -    | -            | Makes `start` and `end` correspond to when the effects are applied                                  |
| `shuffle`       | `sh`        | -      | -    | -            | Shuffles the whole video                                                                            |
| `speed`         | `sp`        | Number | 0.5  | 25           | Slows down or speeds up video                                                                       |
| `start`         | `s`         | Number | 0    | End of Video | Time when video begins, in seconds. (Or start of effect with `selection`)                           |
| `stutter`       | `st`        | Number | 0    | 100          | Adds random stutters to the video                                                                   |
| `timecode`      | `timc`      | Number | 1    | 4            | Messes with the video's timecode metadata. Only applies to Discord bot.                             |
| `ytp`           | `ytp`       | Number | 0    | 100          | Adds random plays and reverses to a video.                                                          |
### Video specific:
| Command         | Shorthand   | Type   | Min  | Max          | Description                                                                                         |
|-----------------|-------------|--------|------|--------------|-----------------------------------------------------------------------------------------------------|
| `acid`          | `acid`      | Number | 1    | 100          | Makes it look like you're on acid                                                                   |
| `bandicam`      | `bndc`      | -      | -    | -            | Adds a Bandicam watermark                                                                           |
| `bottomcap`     | `bcap`      | Text   | 0    | 100          | Bold, centered, white caption at bottom                                                             |
| `bottomcaption` | `bc`        | Text   | 0    | 100          | Bottom caption, in motivational text style                                                          |
| `bottomtext`    | `bt`        | Text   | 0    | 100          | Bottom text in impact font                                                                          |
| `contrast`      | `ct`        | Number | 0    | 100          | Adds extra contrast to the video                                                                    |
| `datamosh`      | `dm`        | Number | 0    | 100          | Corrupts video by removing non-delta frames                                                         |
| `deepfry`       | `df`        | Number | 0    | 100          | Deep fries the video, reduces quality (via added saturation)                                        |
| `fisheye`       | `fe`        | Number | 1    | 2            | Adds a fisheye effect on the video                                                                  |
| `framerate`     | `fps`       | Number | 1    | 30           | Lowers the video's framerate                                                                        |
| `glitch`        | `glch`      | Number | 1    | 100          | Makes the video corrupted                                                                           |
| `hcrop`         | `hcp`       | Number | 1    | 95           | How much to horizontally crop the video, in terms of precent.                                       |
| `hcycle`        | `huec`      | Number | 0    | 100          | Rotates the hue of the video by a certain speed                                                     |
| `hflip`         | `hflp`      | Number | -    | -            | Flips video horizontally.                                                                           |
| `hmirror`       | `hm`        | Number | 1    | 2            | Mirrors horizontal, 1 is the left half, 2 is the right half                                         |
| `holdframe`     | `hf`        | Number | 0.1  | 12           | Makes the video only the first frame, for # of seconds                                              |
| `hscale`        | `hs`        | Number | 0    | 100          | Horizontal scale, sets the vertical resolution                                                      |
| `hue`           | `hue`       | Number | 0    | 100          | Changes the hue of the video                                                                        |
| `hypercam`      | `hypc`      | -      | -    | -            | Adds an "Unregistered Hypercam 2" watermark to the video                                            |
| `invert`        | `inv`       | -      | -    | -            | Inverts video color                                                                                 |
| `lag`           | `lag`       | Number | 1    | 100          | Reverses frames in chunks.                                                                          |
| `normalcaption` | `nc`        | Text   | -    | -            | Standard caption at the top, like in screenshotted twitter posts.                                   |
| `shake`         | `shk`       | Number | 1    | 100          | Shakes the video around                                                                             |
| `sharpen`       | `shp`       | Number | -100 | 100          | Applies a heavy sharpening filter. Negative numbers cause it to become more pixelly.                |
| `topcap`        | `cap`       | Text   | 0    | 100          | Bold, centered, white caption at top                                                                |
| `topcaption`    | `tc`        | Text   | -    | -            | Top caption, in motivational text style                                                             |
| `toptext`       | `tt`        | Text   | -    | -            | Top text in impact font                                                                             |
| `vbr`           | `vbr`       | Number | 0    | 100          | Video bit reduction, worsens quality of video                                                       |
| `vcrop`         | `vcp`       | Number | 1    | 95           | How much to vertically crop the video, in terms of precent.                                         |
| `vflip`         | `vflp`      | Number | -    | -            | Flips video vertically.                                                                             |
| `vmirror`       | `vm`        | Number | 1    | 2            | Mirrors vertically, 1 is the top half, 2 is the bottom half                                         |
| `vreverse`      | `vrev`      | -      | -    | -            | Reverses video                                                                                      |
| `watermark`     | `wtm`       | Number | 0    | 100          | Adds random watermarks to a video. Higher numbers add more.                                         |
| `wave`          | `wav`       | Number | 1    | 100          | Adds a wave to the video; higher values means the wave scrolls faster.                              |
| `waveamount`    | `wava`      | Number | 1    | 100          | Controls amount of waves.                                                                           |
| `wavestrength`  | `wavs`      | Number | 1    | 100          | Controls how big waves are                                                                          |
| `wscale`        | `ws`        | Number | -500 | 500          | Sets the horizontal resolution.                                                                     |
| `zoom`          | `zm`        | Number | -15  | 15           | Zooms towards the middle of the video. Negative values do the same, but more pixellated.            |
### Audio specific:
| Command         | Shorthand   | Type   | Min  | Max          | Description                                                                                         |
|-----------------|-------------|--------|------|--------------|-----------------------------------------------------------------------------------------------------|
| `abr`           | `abr`       | Number | 0    | 100          | Audio Bit Reduction - Reduces audio quality                                                         |
| `areverse`      | `arev`      | -      | -    | -            | Reverses audio                                                                                      |
| `bass`          | `bs`        | Number | 0    | 100          | Bass boost                                                                                          |
| `crush`         | `cr`        | Number | 1    | 100          | Obliterates audio                                                                                   |
| `earrape`       | `er`        | Number | 0    | 100          | Earrapes the video, by making the video very loud and distorted.                                    |
| `music`         | `mus`       | Text   | -    | -            | Music is added using a YouTube video ID (the text after ?watch=). The song must be under 5 minutes. |
| `musicdelay`    | `musd`      | Number | 0    | End of video | Number of seconds corresponding to when the added music starts                                      |
| `musicskip`     | `muss`      | Number | 0    | End of music | Starts the song at a given time of the song (in seconds)                                            |
| `mute`          | `mt`        | -      | -    | -            | Mutes the audio                                                                                     |
| `pitch`         | `pch`       | Number | -100 | 100          | Sets the audio pitch to be higher or lower                                                          |
| `reverb`        | `rvb`       | Number | 0    | 100          | Adds a reverb, or echo, effect                                                                      |
| `reverbdelay`   | `rvd`       | Number | 0    | 100          | Echo response time, 100 means it takes the longest for an echo to bounce back                       |
| `sfx`           | `sfx`       | Number | 1    | 100          | Adds random sound effects                                                                           |
| `wobble`        | `wub`       | Number | 1    | 100          | Makes the audio wobbly.                                                                             |
| `volume`        | `vol`       | Number | 0    | 2000         | Multiplies volume. Higher number results in louder video.                                           |
