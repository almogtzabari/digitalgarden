---
{"dg-publish":true,"permalink":"/notes/how-to-merge-video-files-with-f-fmpeg-on-windows-for-dummies/"}
---


# How to merge video files with FFmpeg on Windows (for dummies)
This is a simple tutorial for how to merge several videos using [[Notes/FFmpeg\|FFmpeg]] without re-rendering (use this if you simply want to merge two clips that were clipped from the save original video).
Follow these steps:
1. [[Notes/How to set up FFmpeg on Windows (for dummies)\|Set up FFmpeg on your Windows machine]].
2. Copy the files you wish to merge to the `bin` folder (explained [[Notes/How to set up FFmpeg on Windows (for dummies)\|here]] in section 2).
3. Create a simple text file called `mylist.txt` inside the `bin` directory. Each line within this file should contain the word `file` and then the name of your file. For example: 
	```
	file 'my_first_file.mp4'
	file 'my_second_file.mp4'
	file 'my_last_file.mp4'
	```
4. Save the text file and close it.
5. In the terminal, run: `ffmpeg -f concat -safe 0 -i mylist.txt -c copy output.mp4`.

`output.mp4` is your merged file.
