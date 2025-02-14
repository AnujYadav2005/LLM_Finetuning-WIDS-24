# Financial Chatbot using Fine-Tuned LLM

[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Model-yellow)](https://huggingface.co/your-username/model-name)
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/repo-name/blob/main/LLM_Finetuning.ipynb)

A question-answering chatbot specialized in financial domain queries, built by fine-tuning Google's Flan-T5 model on custom financial data.

## 📌 Overview
- Fine-tuned LLM for financial Q&A
- Web-scraped dataset from Indian financial sources
- Gradio interface for user interaction
- Quantization & LoRA for efficient training

## ✨ Features
- Answers questions about:
  - Company financials
  - Stock performance
  - Market trends
  - Quarterly results
- Context-aware responses
- Optimized for Indian financial sector

## 🛠️ Installation
```bash
git clone https://github.com/your-username/financial-chatbot.git
cd financial-chatbot
pip install -r requirements.txt
```

## 📁 Requirements
```text
transformers==4.40.2
datasets==2.19.0
gradio==4.27.0
accelerate==0.29.3
bitsandbytes==0.43.1
peft==0.11.1
```

## 🚀 Usage
Run the chatbot interface:
```bash
python app.py
```
Access via Gradio URL

## 📊 Dataset
**Sources:** Moneycontrol, Economic Times

**Size:** 10,000 Q&A pairs

**Structure:**
```json
{
  "question": "What is NVIDIA's current market strategy?",
  "answer": "NVIDIA's platform strategy brings together hardware...",
  "context": "NVIDIA has a platform strategy...",
  "ticker": "NVDA",
  "filing": "2023_10K"
}
```

## 🤖 Model Training
**Base Model:** `google/flan-t5-small`

**Fine-tuning Parameters:**
- **Learning Rate:** 2e-5
- **Batch Size:** 4
- **Epochs:** 5
- **Quantization:** 4-bit

**LoRA Configuration:**
- **Rank:** 8
- **Alpha:** 32
- **Dropout:** 0.1

## 📈 Evaluation
| Metric   | Score |
|----------|-------|
| ROUGE-1  | 0.449 |
| ROUGE-2  | 0.346 |
| ROUGE-L  | 0.442 |
| Inference Time | 2-8s |

## 🖥️ Interface
Gradio Interface

## 🧠 Model Architecture
```mermaid
graph TD
    A[User Question] --> B(Input Encoding)
    B --> C[Fine-Tuned Flan-T5]
    C --> D[Response Generation]
    D --> E[Output Decoding]
    E --> F[Formatted Answer]
```

## 🚧 Challenges
- Dataset cleaning from web-scraped sources
- Quantization/LoRA implementation
- Response time optimization
- Handling financial terminology

## 📜 License
MIT License - See [LICENSE](LICENSE)

## 🙏 Acknowledgments
- Hugging Face Transformers Library
- Google for Flan-T5 model
- Moneycontrol/Economic Times for data

## 📧 Contact
**Anuj Yadav** - yadav.anuj051120@gmail.com

---
### **How to Use This README:**
1. Replace placeholder values (`your-username`, `model-name`, etc.)
2. Add actual interface screenshot URL
3. Update evaluation metrics with your final results
4. Verify package versions match your environment
5. Add any project-specific implementation details
6. Include a proper LICENSE file in your repository
