# LangChain Q&A Chatbot 🤖

A question-answering chatbot built with **LangChain** and **HuggingFace**, featuring a **Gradio** web interface for interactive Q&A. This project explores LangChain's prompt templating and LLM chain orchestration using open-source models.

---

## Features

- **Natural Language Q&A** — Ask any question and get step-by-step reasoning responses
- **LangChain Orchestration** — Uses LangChain's `LLMChain` and `PromptTemplate` for structured prompt management
- **HuggingFace Integration** — Powered by `google/flan-t5-xxl` via HuggingFace Hub
- **Gradio UI** — Simple, interactive web interface to query the model in real time

---

## Tech Stack

| Component | Technology |
|---|---|
| LLM Framework | LangChain |
| Model | Google Flan-T5-XXL (via HuggingFace Hub) |
| UI | Gradio |
| Language | Python (Jupyter Notebook) |

---

## Setup & Installation

### Prerequisites
- Python 3.8+
- HuggingFace account + API token ([get one here](https://huggingface.co/settings/tokens))

### Install Dependencies

```bash
pip install langchain huggingface_hub gradio
```

### Set Your HuggingFace API Token

```python
import os
os.environ['HUGGINGFACEHUB_API_TOKEN'] = 'your_token_here'
```

---

## Usage

1. Clone the repo and open the notebook:

```bash
git clone https://github.com/bhavanachinnari/Langchain.git
cd Langchain
jupyter notebook
```

2. Run all cells in the notebook
3. A Gradio interface will launch at `http://127.0.0.1:7860`
4. Type any question into the input box and get an answer

---

## How It Works

1. A `PromptTemplate` structures the input question with a chain-of-thought instruction: *"Let's think step by step"*
2. The prompt is passed to `HuggingFaceHub` which calls the `flan-t5-xxl` model via API
3. The `LLMChain` manages the prompt → model → response pipeline
4. Gradio wraps the chain in a simple web UI for interactive querying

---

## Example Output

```
Question: What is the capital of France?
Answer: Paris is the capital of France. Paris is located in the Île-de-France region...

Question: New Delhi is capital of which country?
Answer: New Delhi is the capital of India. India is a country in South Asia...
```

---

## Notes

- This is an **introductory LangChain project** built to explore prompt engineering and LLM chain orchestration
- The HuggingFace API token in the notebook has been rotated — replace it with your own before running
- For production use, store API tokens in environment variables or `.env` files, never hardcoded

---

## Dependencies

```
langchain
huggingface_hub
gradio
```
