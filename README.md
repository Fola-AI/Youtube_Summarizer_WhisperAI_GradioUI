# YouTube Video Summarizer & Insight Extractor 🎬
This project leverages OpenAI's Whisper model for speech-to-text transcription and GPT-4 for intelligent content analysis.



An AI-powered tool that automatically transcribes YouTube videos and generates intelligent summaries and insights, with a special focus on interview preparation and question extraction.
**📋 Overview**
This project leverages OpenAI's Whisper model for speech-to-text transcription and GPT-4 for intelligent content analysis. It's particularly useful for extracting interview questions from videos and generating professional, STAR-method responses suitable for job interviews.
**✨ Features**

YouTube Audio Download: Automatically downloads audio from any YouTube video URL
High-Quality Transcription: Uses OpenAI's Whisper Large V3 model for accurate speech-to-text conversion
Intelligent Analysis: Extracts questions and generates professional interview-style answers using GPT-4
STAR Method Formatting: Behavioral questions are answered using the Situation, Task, Action, Result framework
User-Friendly Interface: Clean Gradio web interface for easy interaction
Downloadable Results: Export both transcripts and analysis as text files
GPU Acceleration: Supports CUDA for faster processing when available

**🔧 Prerequisites**

Python 3.12+
Google Colab account (for the notebook version)
OpenAI API key
GPU runtime recommended (for faster Whisper processing)

**📦 Installation**
bashpip install yt-dlp gradio openai ffmpeg-python transformers accelerate librosa

**🚀 Usage**
Google Colab Setup

Open the notebook in Google Colab
Add your OpenAI API key to Colab Secrets:

Go to the key icon (🔑) in the left sidebar
Add a new secret named OPENAI
Paste your OpenAI API key as the value


Run all cells to launch the Gradio interface

Using the Interface

Paste a YouTube video URL in the input field
Click "Process Video"
Wait for the processing to complete (time depends on video length)
View the transcript and AI-generated insights
Download the results as text files if needed

**🏗️ How It Works**
1. Audio Extraction

Uses yt-dlp to download the best quality audio from YouTube
Converts audio to WAV format for optimal processing

2. Transcription

Employs OpenAI's Whisper Large V3 model
Implements chunking for long-form audio (30-second segments)
Runs on GPU when available for faster processing

3. AI Analysis

Sends transcript to GPT-4 for intelligent processing
Extracts all questions from the content
Generates professional interview-style responses:

Behavioral Questions: Uses STAR method (Situation, Task, Action, Result)
Technical Questions: Provides expert-level, detailed responses



4. Output Generation

Displays results in the Gradio interface
Saves transcript and analysis as downloadable text files

**🛠️ Technologies Used**

yt-dlp: YouTube video/audio downloading
OpenAI Whisper: State-of-the-art speech recognition
OpenAI GPT-4: Advanced language model for content analysis
Gradio: Web UI framework
PyTorch: Deep learning framework
Transformers: Hugging Face library for model management
Librosa: Audio processing library

**⚠️ Limitations & Notes**

Requires an active OpenAI API key (costs apply for GPT-4 usage)
Processing time depends on video length and GPU availability
Whisper model download (~3GB) required on first run
Audio quality affects transcription accuracy
Best results with clear speech and minimal background noise

**📄 File Outputs**

transcript.txt: Complete transcription of the video
summary_insights.txt: AI-generated analysis with questions and professional answers

**🔒 Privacy & Security**

API keys are stored securely in Colab Secrets
Audio files are processed locally and temporarily
No data is permanently stored after processing

**💡 Use Cases**

Interview Preparation: Extract questions from interview prep videos
Educational Content: Summarize lectures and tutorials
Meeting Analysis: Transcribe and analyze recorded meetings
Content Creation: Generate insights from video content
Research: Quick extraction of key information from video sources

**🤝 Contributing**
Feel free to open issues or submit pull requests for improvements.
📝 License
This project is open source. Please ensure compliance with YouTube's Terms of Service and OpenAI's usage policies when using this tool.

**🙏 Acknowledgments**

OpenAI for Whisper and GPT models
Hugging Face for the Transformers library
Gradio team for the excellent UI framework


**Note: This tool is for educational and personal use. Always respect copyright and content creator rights when processing videos.**
