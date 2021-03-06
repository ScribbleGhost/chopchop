# 📽🪓 ChopChop

ChopChop is a a user script for [mpv](https://github.com/mpv-player/mpv) media player that allows you to easily cut out parts of video files without re-transcoding or affecting the original quality. The script will leave the original video untouched.![illustration](https://i.imgur.com/2p5ndsA.png)

## Requirements

- [FFMpeg](https://ffmpeg.org/) - If you are using Windows you will have to [add it to PATH](https://scribbleghost.net/2020/07/05/add-environment-variables-in-windows-10/).
- [mpv](https://github.com/mpv-player/mpv) media player.

## Installation

- Make sure you have MPV
- Make sure you have FFmpeg installed or added to PATH.
- Put chopchop.lua file in the scripts folder for mvp:
  - GNU/Linux or macOS: `~/.config/mpv/scripts/`
  - Windows: `%appdata%/mpv/scripts/`

## How to use it

The script runs [FFMpeg](https://ffmpeg.org/) to do the job for you. All you have to do is to:
- Open a video file in mpv.
- Decide if you want audio or not. If you don't want audio, hit <kbd>a</kbd>.
- Find a point in thime where you want to start the clip extraction.
- Hit <kbd>c</kbd> to set the start point.
- Find an end point and hit <kbd>c</kbd> again to to set the end of the clip.
- FFMpeg should now start working for you. The clip will be saved in the user folder together with a log file.

You can also exclude audio by hitting the <kbd>a</kbd> button once before you select the clip.

## Limitations

- Extracted videos does not include subtitles.
  - Since I can't really wrap my head around how mapping works in FFMpeg yet, I haven't found a suitable way to include subtitles.
- Exported clips can only be saved to the "home" directory. On Windows that is `C:\Users\your_username\`.
  - Since I don't really care to learn Lua right now, I will leave it as it is. If you know a way to write a relative path to the desktop folder (that works for Win/Linux and MacOS) please give me a shout. I will gladly add it to the code.

___

*The script is 99% the work of [Kagami Hiiragi](https://github.com/Kagami) [mpv_slicing](https://github.com/Kagami/mpv_slicing) script. I practically stole it and slightly edited it a little. So don't praise me 😉*
