
# 💩 Bad Quality Stream - Make your streams funny
    ffmpeg -f x11grab -framerate 5 -video_size 1366x768 -i :0.0 -f pulse -i default -c:v libx264 -preset ultrafast -crf 51 -maxrate 30k -bufsize 5000k -g 60 -vf format=yuv420p -c:a aac -b:a 8k -b:v 30k -f flv *STREAM URL*
Replace  \*STREAM URL* with the stream url. Example: `rtmp://a.rtmp.youtube.com/live2/exam-ple-rtmp-key`.

You can also change the resolution by replacing 1366x768 with any resolution you want.
