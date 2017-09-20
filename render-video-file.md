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

