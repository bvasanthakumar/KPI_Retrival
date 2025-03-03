# 📊 KPI Retrieval Approaches

## 📝 Introduction
Key Performance Indicators (KPIs) are essential for tracking and evaluating performance across various industries. However, extracting relevant KPIs from unstructured text is challenging due to variations in terminology, phrasing, and context.

This project explores multiple Natural Language Processing (NLP) approaches for automated KPI retrieval, analyzing their effectiveness based on accuracy, robustness, and computational efficiency.

## 🚀 Approaches to Solve the Problem

### 1️⃣ NER + Fuzzy Matching 🔍
**Description:** Uses Named Entity Recognition (NER) to extract KPI-related entities and applies fuzzy string matching to find the closest match.

✅ **Pros:** Works well for exact or near-matching entities.
❌ **Cons:** Fails when the KPI is expressed using synonyms or paraphrases.

**Performance Ranking:** 🥉 (3rd Place)

### 2️⃣ Fine-tuned NER + Fuzzy Matching 🎯
**Description:** Fine-tunes the spaCy NER model with a KPI-specific dataset for improved entity recognition and fuzzy matching.

✅ **Pros:** Enhances entity extraction.
❌ **Cons:** Overfitting to a specific KPI list reduces effectiveness.

**Performance Ranking:** 🏅 (5th Place)

### 3️⃣ TF-IDF + Cosine Similarity 📏
**Description:** Uses TF-IDF (Term Frequency-Inverse Document Frequency) to convert text into numerical vectors and applies cosine similarity for KPI matching.

✅ **Pros:** Captures textual similarities well.
❌ **Cons:** Cannot recognize synonyms.

**Performance Ranking:** 🥈 (2nd Place)

### 4️⃣ TF-IDF + Cosine Similarity + Word2Vec 🤖
**Description:** Enhances TF-IDF similarity by integrating Word2Vec embeddings to capture semantic relationships between words.

✅ **Pros:** Recognizes contextual meaning.
❌ **Cons:** Sometimes retrieves incorrect KPIs due to ambiguity.

**Performance Ranking:** 🏅 (4th Place)

### 5️⃣ TF-IDF + Cosine Similarity + WordNet (Synonyms) 🔥
**Description:** Incorporates WordNet synonyms to improve TF-IDF-based matching, allowing better recognition of paraphrased KPIs.

✅ **Pros:** Best accuracy due to synonym recognition.
❌ **Cons:** Computationally intensive.

**Performance Ranking:** 🥇 (1st Place)

## 🏆 Performance Summary
| Approach | Ranking | Strengths | Weaknesses |
|----------|--------|------------|-------------|
| **NER + Fuzzy Matching** | 🥉 3rd | Simple, efficient | Fails with paraphrased KPIs |
| **Fine-tuned NER + Fuzzy Matching** | 🏅 5th | More accurate entity recognition | Still depends on fuzzy matching |
| **TF-IDF + Cosine Similarity** | 🥈 2nd | Good for exact matches | Cannot handle synonyms |
| **TF-IDF + Word2Vec** | 🏅 4th | Captures contextual meaning | Requires a large dataset |
| **TF-IDF + WordNet** | 🥇 1st | Best accuracy with synonyms | Computationally intensive |

## 📂 Project Setup
### Prerequisites
- Python 🐍
- `spaCy` (for NER)
- `fuzzywuzzy` (for fuzzy matching)
- `scikit-learn` (for TF-IDF & Cosine Similarity)
- `gensim` (for Word2Vec)
- `nltk` (for WordNet Synonyms)

### Installation
```bash
pip install spacy fuzzywuzzy scikit-learn gensim nltk
```

### Running the Project
1. Load the dataset 📂
2. Choose a KPI retrieval approach ⚙️
3. Process input text and retrieve relevant KPI 🎯
4. Evaluate accuracy and performance 📊

## 📌 Conclusion
Through comparative analysis, the **TF-IDF + Cosine Similarity + WordNet (Synonyms) approach** emerges as the best solution for KPI retrieval, enabling organizations to enhance decision-making with AI-driven solutions. 🚀

