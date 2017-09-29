## Adobe After Affects video rendering
Use h264 codec  
80% quality

## Convert file to proper encoding and quality
quality ref: http://williamyaps.blogspot.fr/2017/01/ffmpeg-encoding-h264-decrease-size.html  
scaling: https://trac.ffmpeg.org/wiki/Scaling%20(resizing)%20with%20ffmpeg  

- **scaling half-size**  
`ffmpeg -i input.mp4 -c:v libx264 -crf 23 -vf scale=iw*.5:ih*.5  output.mp4`  

- **scaling to desired size**  
`ffmpeg -i input.mp4 -c:v libx264 -crf 23 -vf scale=540:960  output.mp4`  

- map extension to same extension  
`find -name "*.mp4" -exec ffmpeg -i {} -c:v libx264 -crf 23 -vf scale=540:960  ./output/{}`  

- map extension to another extension  
`find -name "*.mp4" -exec bash -c 'ffmpeg -i "{}" -c:v libx264 -crf 23 -vf scale=540:960  "./output/${0/.mp4}.avi"' {} \;`

- convert videos to mp3 audio codec (works only on android...)  
`find -name "*.mp4" -exec ffmpeg -i {} -acodec mp3 ./output/{} \;`

- convert videos to 48KHz! (works on iOS and Android!!)  
`find -name "*.mp4" -exec ffmpeg -i {} -ar 48000 ./output/{} \;`  

android doc  
https://developer.android.com/guide/topics/media/media-formats.html#audio-formats  
iOS doc  
https://developer.apple.com/library/content/documentation/Miscellaneous/Conceptual/iPhoneOSTechOverview/MediaLayer/MediaLayer.html

NB: **on mac OS X use gfind** instead of find to access -name property from findutils (brew install findutils)


