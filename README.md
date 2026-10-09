# Speech-to-Reasoning Pipeline with OpenAI Whisper and 4-Bit Quantized LLM

An end-to-end machine learning pipeline implemented in Google Colab that converts spoken audio into text via OpenAI Whisper and feeds the transcription into a dynamically 4-bit quantized Mistral-7B Large Language Model for context-aware logical reasoning[cite: 1]. Developed as part of the internship program at Arch Technologies.

## Overview

The objective of this project is to create a resource-efficient speech-to-intelligence pipeline optimized for environments with limited VRAM (such as Google Colab T4 GPUs). The system automates audio format conversion, performs high-accuracy speech transcription, and executes low-footprint LLM inference using 4-bit quantization.

## Pipeline Architecture

1. **Audio Ingestion and Conversion**: Uploads audio/video files and converts them into standardized 16kHz mono `.wav` files using FFmpeg[cite: 1].
2. **Automatic Speech Recognition (ASR)**: Processes the extracted audio with OpenAI Whisper (`small` model variant) to generate text transcripts[cite: 1].
3. **Structured Prompt Generation**: Wraps the transcribed text into a logical reasoning prompt template[cite: 1].
4. **Quantized LLM Inference**: Loads `unsloth/mistral-7b-bnb-4bit` utilizing 4-bit quantization and generates step-by-step reasoning outputs[cite: 1].

## Technical Stack

* **Environment**: Google Colab (Tesla T4 GPU)[cite: 1]
* **Audio Processing**: OpenAI Whisper, FFmpeg, ffmpeg-python[cite: 1]
* **Model Quantization and Inference**: Unsloth, Transformers, PyTorch, BitsAndBytes[cite: 1]

## Getting Started

1. Open the Jupyter Notebook (`taskkk4.ipynb`) inside Google Colab with a GPU runtime enabled[cite: 1].
2. Run the dependency installation cell to load PyTorch, Whisper, Unsloth, and associated packages[cite: 1].
3. Execute the cells sequentially to upload your audio sample, run the transcription, load the quantized model, and produce the reasoned output[cite: 1].

## License

This project was developed for professional training and evaluation purposes during the Arch Technologies internship.
