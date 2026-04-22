# Mental-Health-Response-NLP-with-Fine-tuned-DistilGPT-2
Fine-tuning DistilGPT-2 on a mental health conversation dataset to generate empathetic therapist-style responses to patient queries.
# 🧠 Mental Health Response Generation — NLP Fine-tuning Project

A natural language processing project that fine-tunes **DistilGPT-2** 
(a lightweight GPT-2 variant) on a mental health conversation dataset 
to generate contextually appropriate, therapist-style responses to patient queries.

## 📌 Overview

This project explores the use of generative language models in the mental 
health domain. A pre-trained DistilGPT-2 model is fine-tuned on 
patient–therapist dialogues, teaching it to respond empathetically to 
mental health-related prompts.

## 🔧 How It Works

1. **Data Preparation** — Loads a mental health conversation CSV dataset, 
   cleans whitespace, and formats each entry using special tokens:
   `<|patient|>` and `<|therapist|>`.
2. **Train/Test Split** — 95% training / 5% test split, saved as `.txt` files.
3. **Baseline Evaluation** — Generates sample responses using the 
   pre-trained (untuned) DistilGPT-2 model.
4. **Fine-tuning** — Runs `run_lm_finetuning.py` via a bash script to 
   fine-tune the model for 105 epochs using causal language modeling.
5. **Post-tuning Evaluation** — Compares model outputs before and after 
   fine-tuning on test set examples and custom prompts.

## 🛠️ Tech Stack

- Python, Pandas
- Hugging Face Transformers (`distilgpt2`)
- Google Colab (GPU fine-tuning)
- PyTorch

## 💡 Example

**Input:** `"Why is everything hard?"`  
**Output:** A generated therapist-style response from the fine-tuned model.

## ⚠️ Disclaimer

This project is for **research and educational purposes only**. 
The generated responses are not a substitute for professional mental 
health care or advice.
