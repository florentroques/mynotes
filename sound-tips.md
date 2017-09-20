## Loop mp3
mp3 format is not designed for loops  
explanation: https://www.compuphase.com/mp3/mp3loops.htm  
python script attempt: https://github.com/tom-seddon/bin#make_looping_mp3  
(didn't work when tried)

=> wav format supports loop

## convert wav to mp3
`ffmpeg -i input.wav -codec:a libmp3lame -qscale:a 2 output.mp3`  

Control quality with -qscale:a (or the alias -q:a). Values are encoder specific, so for libmp3lame the range is 0-9 where a lower value is a higher quality. 0-3 will normally produce transparent results, 4 (default) should be close to perceptual transparency, and 6 produces an "acceptable" quality. The option -qscale:a is mapped to the -V option in the standalone lame command-line interface tool.  

see more https://trac.ffmpeg.org/wiki/Encode/MP3

## detect sound volume
`ffmpeg -i input.wav -filter:a volumedetect -f null /dev/null`

## normalize audio volume
see https://superuser.com/questions/323119/how-can-i-normalize-audio-using-ffmpeg  
ffmpeg ref: https://trac.ffmpeg.org/wiki/AudioVolume  
ffmpeg-normalize: https://github.com/slhck/ffmpeg-normalize  

several options:  
- `ffmpeg -i input.wav -filter:a loudnorm output.wav`
- `ffmpeg-normalize -b tamtam-loop16bit.wav`
- use [Levelator tool](http://www.conversationsnetwork.org/levelator) (see below)

Normalize a number of MP4 files to EBU R128 normalization and merge the audio stream back into the MP4 files, in a new directory called normalized:  
`ffmpeg-normalize -vuofb *.mp4`  
( `ffmpeg-normalize --verbose --merge --dir --force --ebu *.mp4` )

previous command but merging the audio back in using the libfdk_aac encoder with 192 kBit/s CBR  
`ffmpeg-normalize -vuofb -a libfdk_aac -e "-b:a 192k" *.mp4`

set the sample rate to a normal value (-b/--ebu: the sample rate of the input file will be changed, which some players do not support)
`ffmpeg-normalize -vuofb -e "-ar 44100" *.mp4`


## sound normalization info
New sound unit LUFS (Loudness units relative to Full Scale) - related to EBU R128 algorithm

- Youtube: videos normalized to -13LUFS  
see http://productionadvice.co.uk/youtube-loudness/

- Spotify: songs normalized to -14LUFS  
see http://productionadvice.co.uk/spotify-reduced-loudness/

==> Normalize to -13LUFS for now

## Tools

- **Levelator**  
http://www.conversationsnetwork.org/levelator  
leveler that corrects for medium-term variations in loudness instead of the short-term and long-term variatons processed by compressor/limiters and normalizers

- **r128x**  
https://github.com/audionuma/r128x  
loudness measurement of files on Mac OSX 

## Loop sound (or video)
```sh
for i in {1..10}; do printf "file '%s'\n" input.mp3 >> mylist.txt; done
ffmpeg -f concat -i mylist.txt -c copy output.mp3
```

## LUFS Meter
https://youlean.co/youlean-loudness-meter/  
Installed in Audacity  
Top Menu > Effect > Scroll to bottom of bottom :)
