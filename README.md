# speech-to-reasoning-pipeline
An end-to-end machine learning pipeline built in Google Colab that transcribes audio (.mp4/.wav) using OpenAI Whisper and routes the text through a dynamically 4-bit quantized Mistral-7B LLM (via Unsloth) for low-VRAM, context-aware logical reasoning.
