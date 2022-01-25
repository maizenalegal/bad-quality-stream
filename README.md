# 💩 Bad Quality Stream - Make your streams funny
    ffmpeg -f x11grab -framerate 5 -video_size 1366x768 -i :0.0 -f pulse -i default -c:v libx264 -preset ultrafast -crf 51 -maxrate 1k -bufsize 5000k -g 60 -vf format=yuv420p -c:a aac -b:a 1k -b:v 1k -f flv *STREAM URL*
   Replace  \*STREAM URL* with the stream url. You can also change the resolution by replacing 1366x768 with any resolution you want.
