# List of yt-dlp / youtube_dl arguments

*if you are using youtube_dl instead of yt-dlp just replace the "yt-dlp" at the beginning to youtube_dl ( some things might not work as expect )*

## download mp3
```
yt-dlp -f ba -x --audio-format mp3 <video link>
```

## download video 720p with audio

*this requires ffmpeg to be installed on your computer*

```
yt-dlp -f 247+251 --merge-output-format mp4 <video link>
```