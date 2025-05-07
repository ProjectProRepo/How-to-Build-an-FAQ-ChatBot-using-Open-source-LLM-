# PDF-to-Quiz Generator using Mistral-7B-Instruct

Turn any large PDF (like a textbook or research paper) into a short quiz using an open-source LLM!

This simple Gradio app allows you to upload a PDF, enter a topic (e.g., "Recursion"), and get a 3-question multiple-choice quiz generated from the most relevant section of the document.

---

##  Overview

This app:

- **Loads** the [Mistral-7B-Instruct](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.1) model using Hugging Face Transformers.
- **Accepts a PDF upload** (up to ~22MB).
- **Extracts text** from the entire document.
- **Performs keyword search** to find the most relevant section based on the input topic.
- **Selects a ~2,000 character window** of the relevant content.
- **Prompts the LLM** to generate 3 multiple-choice questions with 4 options and correct answers.
- **Displays the quiz** instantly using Gradio.

---

## 🛠 Installation

Make sure you have Python 3.8+ installed, then run:

```bash
pip install gradio transformers accelerate pypdf PyPDF2 bitsandbytes
```


## Model Details

- **Model**: `mistralai/Mistral-7B-Instruct-v0.1`  
- **Optimized for**: Conversational instruction-following tasks  
- **Runs in**: 8-bit mode using `bitsandbytes` for efficient performance on consumer GPUs

---
## Usage
Run the app with:

```bash
python app.py
```
Then open the link in your browser to:
-- Upload a PDF file.
-- Enter a topic (e.g., “Sorting algorithms”).
-- View the generated quiz.

---

##  Tip

Use clearly structured academic PDFs or well-formatted notes for better quiz quality. Clean text improves LLM output.

---

## License

This project is licensed under the **MIT License**. Use it freely, adapt it, and share improvements!

---

## Credits

- [Mistral-7B-Instruct](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.1) by Mistral AI  
- [Gradio](https://gradio.app/) for the frontend  
- [ProjectPro](https://projectpro.io/) for inspiring end-to-end GenAI project ideas
