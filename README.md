# 🧠 AI-Powered Fake News Detection System

An advanced fake news detection system combining state-of-the-art NLP and graph-based deep learning techniques. This project uses RoBERTa, GNN (Graph Neural Networks), and HAN (Hierarchical Attention Networks) to classify news articles as **real** or **fake** with high accuracy.

---

## 🚀 Features

- 🔎 **Fake News Classification** using a hybrid model (RoBERTa + GNN + HAN)
- 🌍 **Multilingual Support** via Google Translate
- ✂️ **Summarization** using BART model
- 💬 **Sentiment Analysis** using `cardiffnlp/twitter-roberta-base-sentiment`
- 🎙️ **Audio Input Support** (speech-to-text via Google Speech API)
- 📊 **Fake Probability Score** (outputs percentage fake)
- 🤖 **Telegram Bot Interface** connected via Flask API
- 📝 **User Feedback System** (collects user opinion on predictions)

---

## 📂 Dataset

- **ISOT Fake News Dataset**
  - `True.csv`: Real news articles
  - `Fake.csv`: Fake news articles
  - Total: ~44,000 articles
- Columns: `title`, `text`

---

## 🧠 Model Architecture

### 1. **RoBERTa**
- Extracts deep contextual embeddings from input text

### 2. **GNN (Graph Neural Network)**
- Captures structural and semantic relationships in the article

### 3. **HAN (Hierarchical Attention Network)**
- Focuses attention at both word and sentence level

These are combined in a hybrid architecture for robust fake news classification.

---

## 🛠️ Technologies Used

- `Python`
- `Flask` (API and Web Interface)
- `transformers` (RoBERTa, BART)
- `torch` / `torch_geometric`
- `Google Translate API`
- `Google Speech API`
- `Telegram Bot API`
- `ISOT Fake News Dataset`

---

## 🖥️ System Flow

```mermaid
graph TD
A[User Input: Text / Audio / Image] --> B[Language Detection]
B --> C[Translate to English (if needed)]
C --> D[Summarization using BART]
D --> E[Fake News Prediction (RoBERTa + GNN + HAN)]
E --> F[Sentiment Analysis (RoBERTa)]
E --> G[Fake Score % Output]
F --> H[Show Result + Feedback Option]
