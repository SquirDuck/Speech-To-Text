📖 Overview
This project is designed to demonstrate:

Audio Data Handling: Loading .wav files using scipy.

Signal Processing: Understanding the difference between Time Domain (Amplitude) and Frequency Domain (Spectrum) analysis using Fast Fourier Transform (FFT).

ASR Implementation: Applying Automated Speech Recognition (ASR) to transcribe spoken words from emotional speech datasets.

📂 Datasets
The notebook automatically downloads the following datasets using kagglehub:

Speech Emotion Recognition En: Contains subsets like RAVDESS and SAVEE.

Source: dmitrybabko/speech-emotion-recognition-en

Toronto Emotional Speech Set (TESS): A set of audio files focusing on emotional speech.

Source: phucduck/toronto-emotional-speech

⚙️ Installation & Prerequisites
To run this notebook, you need a Python environment (Python 3.7+ recommended) with the following libraries installed:

Bash

pip install numpy matplotlib scipy SpeechRecognition kagglehub
Note: This notebook is optimized for environments like Kaggle or Google Colab.

📝 Key Components
1. Time Domain Visualization
Visualizes the raw audio signal to observe amplitude changes over time.

Library: scipy.io.wavfile, matplotlib.

Process: Reads the sample rate and signal data, calculates the duration, and plots Amplitude vs. Time (ms).

2. Frequency Domain Analysis (Signal Characterization)
Converts the time-domain signal into the frequency domain using Fast Fourier Transform (FFT). This reveals the dominant frequencies and signal power.

Technique: np.fft.fft.

Output: A Power Spectrum plot showing Signal Power (dB) vs. Frequency (kHz).

3. Speech-to-Text (STT)
Implements transcription using the SpeechRecognition wrapper for the Google Web Speech API.

Class Used: sr.Recognizer().

Workflow:

Load audio file into sr.AudioFile.

Record data into an AudioData instance.

Transcribe using r.recognize_google().
