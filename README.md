# Audio Analysis & Speech-to-Text

📌 **Signal Processing project** for visualizing audio characteristics and generating transcripts using FFT + Google Web Speech API.

A complete pipeline including audio data ingestion, time-domain visualization, frequency-domain characterization (FFT), and automated speech recognition (ASR) for emotional speech datasets.

## Features

* **Time Domain Analysis**: Visualize raw audio signals (Amplitude vs. Time).
* **Frequency Domain Analysis**: Characterize signals using Fast Fourier Transform (FFT) to analyze power spectrum.
* **Speech-to-Text**: Transcribe spoken audio to text using the `SpeechRecognition` library.
* **Dataset Integration**: Auto-download and processing for RAVDESS and TESS emotional datasets.
* **Google API Integration**: Utilizes Google Web Speech API for high-accuracy transcription.

## Notebook

📎 **Kaggle Notebook**: [[Link_to_your_notebook_here](https://www.kaggle.com/code/phucduck/speech-to-text)]

## Project Workflow

* **Input**: Raw Audio (.wav) $\to$ `scipy.io.wavfile`
* **Transformation**: Time Domain $\to$ FFT $\to$ Frequency Domain
* **Recognition**: `sr.AudioFile` $\to$ Google Cloud API $\to$ Text Output

## Datasets

This project utilizes the following datasets via `kagglehub`:
* **RAVDESS**: Ryerson Audio-Visual Database of Emotional Speech and Song.
* **TESS**: Toronto Emotional Speech Set.

## Requirements

```python
!pip install numpy matplotlib scipy SpeechRecognition kagglehub
