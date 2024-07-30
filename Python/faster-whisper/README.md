# Demo using Faster Whisper (tested with Python 3.9.12)

The aim of this script is to test the Text to Speech feature using Whisper model.
The output can be saved as .srt file to serve as a subtitle for video for example.

For this demo I generated the ```audio.wav``` using [Synthesys AI
Studio](https://synthesys.io/italian-text-to-speech/)
Then I converted it using ffmpeg tool using this command

```bash
ffmpeg -i audio.mp3 -ac 1 -ar 16000 audio.wav
````

Having one single audio wave file will reduce the file size and the processing time.

## Setup

```bash
git clone git@github.com:proxium/lab.git
cd lab/Python/faster-whisper
python3.9 -m venv env
source env/bin/activate
env/bin/python3.9 -m pip install --upgrade pip
pip install -r requirements.txt -v --log pip_debug.log
```

## Usage

```bash
python faster.py
```

## Output

The lyrics of the song **Laura non c'è** will be written in the console.

```
Detected language 'it' with probability 1.000000
[0.00s -> 4.00s]  Laura non c'è, è andata via. Laura non è più cosa mia.
[4.00s -> 8.00s]  E te che sei qua e mi chiedi perché? L'amose niente più mi dà.
[8.00s -> 13.00s]  Mi manca da spezzare il fiato. Fa male e non lo sa. Che non mi è mai passata.
```
