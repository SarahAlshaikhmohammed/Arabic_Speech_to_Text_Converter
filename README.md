
# Arabic Speech to Text Converter

This project demonstrates how to convert Arabic speech into text using Python libraries like `speech_recognition`, `pydub`, and others. It processes audio files, splits them into chunks, and transcribes them into text using Google’s Speech Recognition API.

## Features

- Converts Arabic speech from audio files into text.
- Splits large audio files into manageable chunks based on silence detection.
- Supports transcription of large files by processing chunks individually.
- Outputs transcribed text into a `.txt` file.

## Installation

To use this project, you need to install the required libraries. You can do so using the following command:

```bash
pip install pydub pytube speechrecognition google-cloud-storage ffmpeg
```

## How to Use

1. Clone or download this repository.
2. Place the audio file (in Arabic) that you want to transcribe in the working directory.
3. Run the script, and it will process the audio, transcribe it, and save the result as a `.txt` file.

### Example:

```python
# Define the path to your audio file
downloaded_file = "/path/to/audio.wav"

# Transcribe the audio file
transcription = get_large_audio_transcription(downloaded_file, method='silence')
print(transcription)

# Save the transcription to a text file
transcription_df = pd.DataFrame([transcription], columns=['Transcription'])
transcription_df.to_csv('text.txt')
```

In this example, the audio file `audio.wav` is transcribed into text and saved as `text.txt`.

## License

This project is open-source and available under the MIT License.
