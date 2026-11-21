# 🎙️ AI Meeting Minutes Generator

An AI-powered meeting assistant that explores how speech recognition and Large Language Models can transform meeting recordings into structured meeting documentation.

**Project Status:** Educational Prototype

---

## 📌 Project Overview

This project combines Automatic Speech Recognition (ASR) and Large Language Models (LLMs) to explore an automated meeting documentation workflow.

The system converts audio recordings into text using OpenAI Whisper, then uses Meta Llama 3.1 8B Instruct to generate structured meeting minutes from a transcript.

The goal is to reduce manual note-taking and make meeting information easier to review and organize.

## ✨ Key Features

- **Audio Transcription:** Convert meeting recordings into text using Whisper Medium English.
- **AI-Powered Summarization:** Generate structured meeting summaries using Llama 3.1 8B Instruct.
- **Discussion Points:** Organize the main topics discussed.
- **Key Takeaways:** Extract important conclusions.
- **Action Items:** Structure follow-up tasks and their suggested owners.
- **Interactive Interface:** Upload audio files through a Gradio interface and view the transcription.

## 🏗️ Workflow

1. Upload a meeting audio recording.
2. Whisper processes the audio and generates a transcript.
3. The transcript is provided to an LLM.
4. Llama generates structured meeting minutes.
5. The generated content can be reviewed in Markdown format.

## 🧠 Models & Technologies

**Programming Language:** Python
- **Speech Recognition:** OpenAI Whisper Medium (English)
- **LLM:** Meta Llama 3.1 8B Instruct
- **Model Quantization:** BitsAndBytes (4-bit NF4)
- **Deep Learning:** PyTorch
- **Model Framework:** Hugging Face Transformers
- **User Interface:** Gradio
- **Environment:** Google Colab with T4 GPU

## ⚙️ Model Optimization

The Llama model is loaded using 4-bit quantization with the NF4 quantization format.

This configuration helps reduce GPU memory requirements when running the model in a Google Colab environment.

## 🚀 Getting Started

### Requirements

- Python
- Google Colab
- GPU runtime (NVIDIA T4 recommended)
- Hugging Face account with access to the Llama model

### Setup

1. Open the notebook in Google Colab.
2. Select a GPU runtime.
3. Add your Hugging Face access token as a Colab Secret named `HF_TOKEN`.
4. Configure the application authentication secrets (`APP_USER` and `APP_PASSWORD`).
5. Run the notebook cells in order.
6. Upload an audio file through the Gradio interface to generate its transcription.

**Notebook:** [MeetingMinutesProduct.ipynb](./MeetingMinutesProduct.ipynb)

## ⚠️ Current Limitations

- The current speech recognition model is English-focused.
- Meeting minutes generation and audio transcription are implemented as separate notebook stages.
- The current Gradio interface exposes audio transcription; the complete end-to-end minutes generation workflow is not yet integrated into the interface.
- Generated summaries and action items require human review to verify accuracy and task ownership.

## 🔮 Future Improvements

- Integrate transcription and minutes generation into one interface.
- Support multiple languages.
- Add downloadable meeting reports (Markdown and PDF).
- Improve action-item extraction and owner identification.
- Add timestamps and speaker identification.
- Develop a more complete end-to-end application.

## 📚 Learning Outcomes

This project provided hands-on practice with:

- Automatic Speech Recognition (ASR).
- Large Language Model inference.
- Hugging Face Transformers.
- Quantization and GPU memory optimization.
- Prompt engineering for structured outputs.
- Building interactive AI interfaces with Gradio.

---

**Developed as an educational AI engineering project.**
