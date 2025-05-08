# PDF Question Answering Chatbot using Mistral-7B-Instruct

Ask questions directly from any large PDF using an open-source LLM.

This simple Gradio app allows you to upload a PDF, ask a question, and get a relevant, LLM-generated answer based on the document content.

---

## Overview

This app:

- Loads the [Mistral-7B-Instruct](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.1) model using Hugging Face Transformers.
- Accepts a PDF upload (up to ~22MB).
- Extracts text from all pages of the document.
- Splits the text into overlapping chunks for better context matching.
- Finds the most relevant chunk using keyword overlap with the input query.
- Prompts the LLM to generate an answer based on the selected chunk.
- Displays the response using a simple Gradio interface.

---

## Installation

Make sure you have Python 3.8+ installed, then run:

```bash
pip install gradio transformers accelerate pypdf PyPDF2 bitsandbytes
```

## Model Details

- **Model**: `mistralai/Mistral-7B-Instruct-v0.1`  
- **Optimized for**: Instruction-following and QA tasks  
- **Runs in**: 8-bit quantized mode via `bitsandbytes` for resource-efficient inference

---

## Credits

- [`Mistral-7B-Instruct`](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.1) by Mistral AI  
- [Gradio](https://gradio.app/) for building the interface  
- [ProjectPro](https://projectpro.io/) for end-to-end GenAI project inspiration


