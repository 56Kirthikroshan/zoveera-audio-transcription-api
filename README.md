# Zoveera Audio Transcription API

An AI-powered audio processing API that performs transcription, translation, and sentiment analysis using modern machine learning models.

## Project Overview

Zoveera is a FastAPI-based backend service that accepts audio files and processes them using speech recognition and NLP techniques. The system transcribes speech, translates the text if required, performs sentiment analysis, and stores results in a MongoDB database.

## Features

- Audio transcription using Whisper
- Language translation
- Sentiment analysis using NLP models
- Word Error Rate (WER) evaluation
- MongoDB storage for processed results
- REST API endpoints using FastAPI
- Automatic API documentation via Swagger UI

## Tech Stack

- Python
- FastAPI
- Whisper Speech Recognition
- Transformers (Hugging Face)
- MongoDB
- PyTorch
- Uvicorn

## API Endpoints

### Health Check

GET /health

Returns service status and database connectivity.

Example response:
{
"service": "Zoveera Audio Transcription API",
"mongodb_status": "connected"
}

### Process Audio

POST /process

Uploads an audio file and returns transcription, translation, and sentiment analysis.

Input:
- Audio file (wav/mp3)

Output:
- Transcription
- Translated text
- Sentiment result
- JSON response stored in database

## Project Structure

zoveera-audio-transcription-api
│
├── app
│ ├── app.py
│ ├── config.py
│ ├── models.py
│ ├── sentiment.py
│ ├── storage.py
│ ├── transcribe.py
│
├── uploaded_audio
├── requirements.txt
├── README.md


## How to Run the Project

1. Clone the repository


git clone https://github.com/56Kirthikroshan/zoveera-audio-transcription-api.git


2. Navigate to the project folder


cd zoveera-audio-transcription-api


3. Install dependencies


pip install -r requirements.txt


4. Run the API server


uvicorn app.app:app --reload


5. Open API documentation


http://127.0.0.1:8000/docs


## Future Improvements

- Real-time speech transcription
- Speaker identification
- Emotion detection from speech
- Docker container deployment
- Cloud deployment

## Author

Kirthik Roshan P  
AI & Data Science Graduate  
