---
{"dg-publish":true,"dg-path":"How to trim a video using FFmpeg (for dummies).md","permalink":"/how-to-trim-a-video-using-f-fmpeg-for-dummies/"}
---



# How to trim a video using FFmpeg (for dummies)
In order to split a video file using [[Notes/FFmpeg\|FFmpeg]] follow these steps:
1. [[Notes/How to set up FFmpeg on Windows (for dummies)\|Set up FFmpeg on your Windows machine]] and open the terminal.
2. Copy the file you want to trim to the `bin` folder (explained [[Notes/How to set up FFmpeg on Windows (for dummies)\|here]] in step 2).
3. In the terminal, type `ffmpeg -i source.mp4 -ss 0 -t 70 -c copy part1.mp4`. 

Let's break down the command from step 3:
- `source.mp4` is your file name. For example: `my_video.mkv`.
- `-ss 0` means start from second number `0`.
- `-t 70` means end at second number `70` (=1 minute and 10 seconds).
- If you wish to cut your video at `28:40` use the formula $28\cdot 60+40=1,720$.
- `-c copy` means to copy all input streams - all parameters related to audio, video (resolution for example), subtitles, etc.
- `part1.mp4` is the name of the output file (what name to give to the trimmed video file).
