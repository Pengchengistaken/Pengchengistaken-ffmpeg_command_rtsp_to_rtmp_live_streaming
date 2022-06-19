# Pengchengistaken-ffmpeg_command_rtsp_to_rtmp_live_streaming
* with this command, it will not invole your server/PC's GPU, so you can run it on low hardware config PC.
* Change "your-rtmp-live-streaming-address-and-access-key" to your application's address and acccess key.

# for windows
```
@echo off  
set INTERVAL= 10
:Again
echo start server
ffmpeg -r 30 -rtsp_transport tcp -i "rtsp://192.168.1.238:554/ch0_0.h264" -vcodec copy -preset:v slower -an -f flv -flvflags no_duration_filesize "your-rtmp-live-streaming-address-and-access-key"
timeout %INTERVAL%
goto Again
```
