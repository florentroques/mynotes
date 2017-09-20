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
