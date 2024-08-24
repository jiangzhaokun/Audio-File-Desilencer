# Audio-File-Desilencer

This tool enables automatic detection, recording, and removal of silent and low-dicibel parts in audio files.


- Batch processing: Capable of processing multiple audio files within a specified folder.  
- Support for both MP3 and WAV formats: Capable of handling audio files in both MP3 and WAV formats.  
- Output timestamps (txt): Generation of timestamp files in milliseconds for both silent and non-silent parts of the audio files.  
- Output extracted non-silent and silent audio segments (mp3): Creation of MP3 format files containing the extracted non-silent and silent parts of the audio.  
- Flexible output file naming: Matching input files with output files based on their filenames.

# Usage
1. Clone the repository
```zsh
git clone https://github.com/jiangzhaokun/Audio-File-Desilencer.git
```

2. Navigate to the project directory
```zsh
cd Audio-File-Desilencer
```

3. Install the required dependencies:
```zsh
pip install -r requirements.txt
```
4. Put all your audio files into the directory "audios"
5. Now run the desilencer using the command line:
By default:
```
python audio_processor.py
```
Add more arguments:
- `input_folder` (optional): The path to the directory of audio files.
- `output_folder` (optional): The path to the directory of output files.
- `min_silence_len` (optional): The minimum duration of silence (in milliseconds) to be considered as a segment of silence (default is 3 seconds).
- `threshold` (optional): The silence threshold in dBFS (decibels relative to full scale) used to distinguish between silent and non-silent segments (default is -35 dBFS).
6. One usage example
```zsh
python audio_processor.py --input_folder ./audios --output_folder ./outputs --min_silence_len 1000 --threshold -50
```
