# 🇳🇵 NepText – A Unified Transformer-Based Web Extension for Nepali Text Intelligence

**NepText** is a unified web-based NLP toolkit that supports **real-time spell correction, grammar checking, Romanized-to-Devanagari transliteration, sentiment analysis**, and **contextual word prediction** for the Nepali language. Built with multilingual transformer models like **mBART**, **BERT**, and **T5**, NepText aims to bridge the digital linguistic gap for Nepali users.

---

## 🎯 Project Objectives

- ✅ Real-time **spelling and grammar correction** for Nepali (Unicode and Romanized)
- ✅ **Bidirectional Romanized–Unicode transliteration**
- ✅ **Sentiment analysis** for Romanized Nepali inputs
- ✅ **Next-word prediction** using n-gram and transformer models
- ✅ Lightweight **web extension** usable across devices

---

## 🧠 Core Technologies

| Component                     | Stack / Tools Used                           |
|------------------------------|----------------------------------------------|
| 🧩 Models                     | mBART, T5, BERT                              |
| 🔠 Spell/Grammar Correction   | T5 (fine-tuned on noisy Nepali corpus)      |
| 🔄 Transliteration            | mBART (Romanized ⇌ Unicode)                 |
| 🧭 Sentiment Classification   | BERT (trained on labeled Romanized comments)|
| 🧠 Word Prediction            | n-Gram models + LLM contextual suggestions   |
| 🎨 Frontend                   | HTML, JavaScript, Tailwind CSS              |
| 🗃️ Local Logging              | SQLite (lightweight offline DB)              |
| ⚙️ Error Matching             | Damerau-Levenshtein Distance Algorithm       |

---
### 🔌 Modules

1. **Input Handler** – Accepts typed input (Unicode or Romanized)
2. **Correction Engine** – Applies spell and grammar checks
3. **Transliterator** – Converts Romanized ↔ Devanagari
4. **Sentiment Analyzer** – Detects sentiment contextually
5. **Word Predictor** – Recommends next word or correction
6. **User Interface** – Chrome Extension or Web UI

### 🧬 Model Training Overview

| Model | Task | Dataset | Strategy |
|-------|------|---------|----------|
| mBART | Transliteration | Romanized-Devanagari pairs | Supervised Seq2Seq |
| T5    | Spell + Grammar Correction | Corrupted ↔ Correct Pairs | Noise injection |
| BERT  | Sentiment Classification | Romanized Comments (Tagged) | Cross-Entropy Loss |

---

## 📦 Features in Action

- 🔄 Convert `ma timilai maya garchu` → `म तिमीलाई माया गर्छु`
- ✅ Correct `मेरो नाम कुशल छा` → `मेरो नाम कुशल छ`
- 📊 Sentiment: `Yo movie ekdam ramailo cha!` → **Positive**
- ✍️ Type: `नेपाल` → auto-completes to `नेपाल एक सुन्दर देश हो।`

---

## 🧰 Installation & Usage

> Web Extension Version Coming Soon...

To run locally (for contributors):
```bash
git clone https://github.com/your-username/neptext.git
cd neptext
npm install
npm run dev
