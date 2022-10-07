# youtube-dl on Ubuntu

There have been problems running yt-dlp on older versions of Ubuntu because of Python version conflicts.

## yt-dlp has a standalone Linux binary now with Python 3.10 built in

```
https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux
```

```
$ sudo wget https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux -O /usr/local/bin/yt-dlp_linux
$ sudo chmod a+rx /usr/local/bin/yt-dlp_linux
$ sudo ln -s /usr/local/bin/yt-dlp_linux /usr/local/bin/yt-dlp

```



