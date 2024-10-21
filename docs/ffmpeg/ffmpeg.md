# List of FFMPEG arguments

### ffmpeg
- make the video shit as much as possible
```
ffmpeg -i input.mp4 -vf "scale=10:10, fps=10" -b:a 500 -b:v 2k -bufsize 2k output.mp4
```

- make the video shit version 2 (with custom bg audio)
```
ffmpeg -i input.mp4 -i bgsong.mp3 -map 0:v -map 1:a -shortest -vf "scale=iw:ih:neighbor, fps=60" -b:a 5000 -b:v 500k -bufsize 100k -preset ultrafast output.mp4
```
(without custom bg audio)
```
ffmpeg -i input.mp4 -vf "scale=iw:ih:neighbor, fps=60" -b:a 5000 -b:v 500k -bufsize 100k -preset ultrafast output.mp4
```



### yt-dlp / youtube_dl

if you are using youtube_dl instead of yt-dlp just replace the "yt-dlp" at the beginning to youtube_dl ( some things might not work as expect )

- download mp3
```yt-dlp -f ba -x --audio-format mp3 <video link>```

- download video 720p with audio
```yt-dlp -f 247+251 --merge-output-format mp4 <video link>```