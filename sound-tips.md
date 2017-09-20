an mp3 file is not easily loopable...   
see https://www.compuphase.com/mp3/mp3loops.htm  

.wav supports loop

## detect sound volume
ffmpeg -i input.wav -filter:a volumedetect -f null /dev/null

## change audio volume
- ratio
ffmpeg -i input.wav -filter:a "volume=1.5" output.wav

- decibels  
ffmpeg -i input.wav -filter:a "volume=10dB" output.wav

## normalize audio volume
see https://superuser.com/questions/323119/how-can-i-normalize-audio-using-ffmpeg  

several options:  
- ffmpeg -i input.wav -filter:a loudnorm output.wav
- ffmpeg-normalize -b tamtam-loop16bit.wav
- use [Levelator tool](http://www.conversationsnetwork.org/levelator) (see below)



## sound normalization info
New sound unit LUFS (Loudness units relative to Full Scale) - related to EBU R128 algorithm

- Youtube: videos normalized to -13LUFS  
see http://productionadvice.co.uk/youtube-loudness/

- Spotify: songs normalized to -14LUFS  
see http://productionadvice.co.uk/spotify-reduced-loudness/

-> Normalize to -13LUFS for now

## Tools

- **Levelator**  
http://www.conversationsnetwork.org/levelator  
leveler that corrects for medium-term variations in loudness instead of the short-term and long-term variatons processed by compressor/limiters and normalizers

- **r128x**  
https://github.com/audionuma/r128x  
loudness measurement of files on Mac OSX 


