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

## sound normalization
New sound unit LUFS (Loudness units relative to Full Scale) - related to EBU R128 algorithm

On Youtube all videos are normalized to -13LUFS  
see http://productionadvice.co.uk/youtube-loudness/

On Spotify songs normalized to -14LUFS  
see http://productionadvice.co.uk/spotify-reduced-loudness/
