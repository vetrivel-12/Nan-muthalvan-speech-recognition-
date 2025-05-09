# Nan-muthalvan-speech-recognition-
Accent-Aware Speech Recognition System for Virtual Assistant
This project implements a real-time accent-aware speech recognition system using deep learning and speaker adaptation techniques. It's designed to improve the performance of voice-based virtual assistants by adapting to different speaker accents and voices.

Features
Real-time speech-to-text transcription using Wav2Vec2
Accent and speaker adaptation using x-vector embeddings from SpeechBrain
RESTful API using Flask for easy integration
Upload audio and get transcribed text and speaker embedding
Supports .wav files sampled at 16kHz
Requirements
Python 3.8+
PyTorch
Transformers
Torchaudio
Librosa
SpeechBrain
Flask
Installation
Clone the repository:
git clone https://github.com/your-username/accent-aware-virtual-assistant.git
cd accent-aware-virtual-assistant
Install dependencies:
pip install -r requirements.txt
If requirements.txt is missing, manually install:

pip install torch torchaudio librosa transformers speechbrain flask
Run the server:
python app/accent_aware_virtual_assistant.py
API Usage
Endpoint:
POST /transcribe

Payload:
Send a .wav file using form-data.

Example using curl:

curl -X POST -F "audio=@sample.wav" http://localhost:5000/transcribe
Response:
{
  "transcription": "Turn on the lights in the kitchen.",
  "speaker_embedding": [0.0412, -0.0133, ...]
}
File Structure
accent-aware-virtual-assistant/
│
├── app/
│   └── accent_aware_virtual_assistant.py
│
├── uploads/
├── pretrained_models/
│   └── spkrec/
├── requirements.txt
├── README.md
└── .gitignore
License
This project is licensed under the MIT License.

end to end speech recognition 2

Real-Time Speech-to-Text Transcription System for Healthcare with Noise Robustness
This Python project implements a real-time speech-to-text transcription system designed specifically for healthcare environments. It uses OpenAI’s Whisper model for transcription and includes noise robustness, medical term normalization, and critical keyword detection.

Features
Real-time microphone recording
Speech-to-text transcription using Whisper (base model)
Noise robustness with live audio stream handling
Normalization of medical terms (e.g., "bp" → "blood pressure")
Keyword detection for important healthcare alerts
Automatic logging of transcriptions with timestamps
Installation
Clone this repository:

git clone https://github.com/your-username/healthcare-stt-whisper.git
cd healthcare-stt-whisper
Install dependencies:

pip install -r requirements.txt
(Optional) Set up a virtual environment:

python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
Usage
Run the main script:

python main_healthcare.py
Output
The system will:

Listen to audio in 5-second intervals
Transcribe the speech
Normalize common medical shorthand
Detect and print alerts for keywords (e.g., "emergency", "blood pressure")
Save all transcriptions in transcription_log.txt
Sample Console Output
[INFO] Recording started. Speak now...
Transcription:
The patient's blood pressure is 130 over 85 and shows signs of diabetic condition.
------------------------------------------------------------
[ALERT] Detected medical terms: blood pressure, diabetic
Example Medical Term Normalization
Detected Term	Normalized Term
bp	blood pressure
sugar level	glucose level
ekg	ECG
covid	COVID-19
diabetes type 1	Type 1 Diabetes
File Structure
healthcare-stt-whisper/
├── main_healthcare.py         # Main Python script
├── requirements.txt           # Dependencies
├── README.md                  # Documentation
├── transcription_log.txt      # Auto-created log of transcriptions
└── .gitignore                 # Common ignored files
Requirements
Python 3.7+
whisper
numpy
sounddevice
soundfile
torch
License
This project is open-source and licensed under the MIT License.

Developed for use in healthcare transcription, telemedicine support, and voice-powered diagnostics.

accent aware speech recognition 3

# Accent-Aware Speech Recognition System
This project implements an Accent-Aware Speech Recognition System using deep learning and speaker adaptation techniques. It aims to improve transcription accuracy for speakers with diverse accents by integrating accent detection and specialized adaptation models.

Features
Deep Learning-Based ASR: Uses state-of-the-art speech recognition models.
Accent Detection Module: Identifies speaker accent to guide the ASR system.
Speaker Adaptation: Fine-tunes models or applies adaptation layers for improved accuracy on accent-specific data.
End-to-End Pipeline: From raw audio input to transcribed text.
Customizable & Extensible: Easily integrate new accents or adaptation strategies.
Project Structure
