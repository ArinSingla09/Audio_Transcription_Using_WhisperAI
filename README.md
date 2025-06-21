# Audio_Transcription_Using_WhisperAI


## Problem Statement
In a digital world dominated by audio content, manual transcription is time-consuming and error-prone. This project aims to develop a web-based application for efficient, accurate, and user-friendly speech-to-text transcription using OpenAI's Whisper model integrated with Streamlit.

## Goals and Scope
### Primary Goal
Develop a user-centric web application for high-fidelity speech-to-text conversion.
### Scope
- Support for MP3 and WAV audio formats.
- Built-in audio preprocessing and resampling.
- Integration with Whisper's inference pipeline.
- Downloadable transcript in .srt format.
### Target Audience
Content creators, educators, researchers, journalists, accessibility advocates, and professionals needing fast, reliable audio transcription.

## Requirements
### Functional Requirements
- Upload MP3 or WAV files.
- Preprocess audio into 16 kHz mono using Librosa.
- Transcribe audio using OpenAI Whisper.
- Display transcribed text in the UI.
- Option to download transcript as .srt.
- Show spinner/progress during transcription.
### Non-Functional Requirements
- Performance: Transcribe ~5-minute files in under 1 minute.
- Usability: Interface accessible to non-technical users.
- Compatibility: Cross-platform support (Windows, macOS, Linux).
- Security: Auto-deletion of temporary files post-processing.
- Maintainability: Modular, documented codebase.
- Scalability: Extensible to cloud-based/multi-user setups.
- Reliability: Conflict-free temporary file handling.

## Project Planning and Scheduling
### Day 1: Requirement & Setup
- Define scope, install Python & FFmpeg, create venv, install dependencies.
### Day 2: UI & Upload Handling
- Build Streamlit UI, handle file uploads & validation, add spinner.
### Day 3: Transcription Logic
- Load model, integrate Librosa, execute transcription, display transcript.
### Day 4: Download & Testing
- Implement download feature, test edge cases, validate inputs.
### Day 5: Documentation & Cleanup
- Modularize code, comment codebase, create README, polish UI.

## Technology Stack
- Python 3.8+
- Streamlit
- OpenAI Whisper
- Librosa
- PyTorch
- tempfile

## Setup Instructions
1. Create virtual environment:
python -m venv venv

2. Activate environment:
- macOS/Linux: `source venv/bin/activate`
- Windows: `venv\Scripts\activate`
3. Install dependencies:
pip install streamlit openai-whisper librosa torch

4. Run application:
streamlit run app.py

## Core Features
- Multi-format upload (MP3 & WAV).
- Live transcription feedback with progress spinner.
- High precision transcription even with noisy inputs.
- Downloadable .srt subtitle files.

## Testing
### Detailed test cases and expected results are documented for:
   - Valid MP3 and WAV uploads.
   - Unsupported formats.
   - FFmpeg installation check.
   - Empty file handling.
   - Download functionality.

## Advantages and Disadvantages
### Advantages
- High transcription accuracy.
- User-friendly interface.
- Supports common audio formats.
- Secure temporary file handling.

### Disadvantages
- Local deployment limitations for scalability.
- Initial setup of Python and FFmpeg required.
- Performance dependent on hardware capabilities.

## Challenges Encountered
- Whisper installation and format compatibility.
- Latency issues with long audio files.
- Effective use of temporary file handling.

## Conclusion
- The WhisperAI Transcription Application offers a robust solution for accurate and efficient audio-to-text conversion. Combining OpenAI's Whisper model with Streamlit provides a reliable platform for various professional and educational applications.

## References
- OpenAI Whisper GitHub : https://github.com/openai/whisper
- Streamlit Documentation : https://docs.streamlit.io/
- Librosa Audio Library : https://librosa.org
- PyTorch : https://docs.pytorch.org/docs/stable/index.html
