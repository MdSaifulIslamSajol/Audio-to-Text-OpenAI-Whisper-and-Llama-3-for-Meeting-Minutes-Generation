Project Summary

This notebook demonstrates an end-to-end pipeline for generating structured meeting minutes from audio recordings using state-of-the-art AI models:

Audio Transcription:
The code uses the OpenAI Whisper model (whisper-1) to transcribe meeting audio files into text. The audio file is uploaded to OpenAI's API, which returns the transcript.

Meeting Minutes Generation:
The transcript is then passed as input to Meta's Llama 3 (meta-llama/Meta-Llama-3.1-8B-Instruct) large language model. The Llama 3 model is prompted to generate detailed meeting minutes, including a summary, key discussion points, takeaways, and action items with owners, all formatted in Markdown.

Pipeline Details:

The code handles authentication for both Hugging Face and OpenAI APIs.
It uses the Hugging Face transformers library for model loading and text generation.
Quantization and efficient memory usage are configured for Llama 3 to enable GPU acceleration.
Attention masks and padding are set to ensure reliable and high-quality text generation.
In summary:
This notebook automates the process of converting meeting audio into well-structured, actionable meeting minutes using Whisper for speech-to-text and Llama 3 for advanced summarization and formatting
