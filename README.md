# 📰 NewsBot Intelligence System 2.0
### Advanced NLP Integration and Analysis Platform
**ITAI2373 | Final Project | Yusuf Shahzad**

---

## 🎯 Project Overview

NewsBot Intelligence System 2.0 is a production-ready AI platform that automatically processes, classifies, and extracts actionable intelligence from news articles at scale. Built on 7 integrated NLP modules, the system takes any news article as input and returns a complete intelligence report — category, sentiment, named entities, topic, summary, keywords, and similar articles — in a single function call.

The system was built entirely on **Google Colab Free Tier** using open-source Python libraries and achieves **97.22% classification accuracy** on the BBC News dataset.

---

## 📊 Key Results

| Metric | Result |
|--------|--------|
| 🏆 Best Classification Accuracy | **97.22%** (Linear SVM Calibrated) |
| 🔄 Cross-Validation Accuracy | **97.71% ± 1.11%** (5-fold) |
| 💪 Average Confidence Score | **92.79%** |
| 📝 Summarization Compression | **86.4%** average reduction |
| 🌍 Languages Supported | **55+** via automatic detection |
| 🏷️ Total Entities Extracted | **8,297** across all articles |
| 📰 Articles Analyzed | **1,440** BBC News articles |
| 🗂️ Categories | **5** (Business, Tech, Politics, Sport, Entertainment) |

---

## 🗂️ Repository Structure

```
ITAI2373-NewsBot-Final/
│
├── 📓 notebooks/
│   ├── 01_Data_Exploration.ipynb          # Data loading, EDA, base NLP pipeline
│   ├── 02_Advanced_Classification.ipynb   # 97.22% classifier with confidence scores
│   ├── 03_Topic_Modeling.ipynb            # LDA + NMF topic discovery
│   ├── 04_Language_Models.ipynb           # Summarization + semantic search
│   ├── 05_Multilingual_Analysis.ipynb     # Language detection + translation
│   ├── 06_Conversational_Interface.ipynb  # Natural language query system
│   └── 07_System_Integration.ipynb        # Unified end-to-end pipeline ⭐
│
├── 📁 src/
│   ├── data_processing/                   # Preprocessing utilities
│   ├── analysis/                          # Classification, sentiment, NER
│   ├── language_models/                   # Summarization, embeddings
│   ├── multilingual/                      # Translation, language detection
│   ├── conversation/                      # Query processing, intent classification
│   └── utils/                             # Visualization, evaluation helpers
│
├── 📁 data/
│   ├── raw/                               # BBC News Train.csv (original dataset)
│   └── processed/                         # newsbot_final.csv (preprocessed)
│
├── 📁 docs/
│   ├── technical_documentation.md         # Architecture and API reference
│   ├── user_guide.md                      # How to use the system
│   └── deployment_guide.md               # Setup and deployment instructions
│
├── 📁 reports/
│   ├── FP_TechnicalDoc_YusufShahzad_ITAI2373.docx
│   ├── FP_ExecutiveSummary_YusufShahzad_ITAI2373.docx
│   ├── FP_ReflectiveJournal_YusufShahzad_ITAI2373.pdf
│   └── FP_Presentation_YusufShahzad_ITAI2373.pptx
│
└── requirements.txt                       # All dependencies with versions
```

---

## 🚀 Quick Start

### 1. Open in Google Colab
Upload any notebook to [Google Colab](https://colab.research.google.com) — no local setup needed.

### 2. Upload the Dataset
In the Colab file panel (folder icon on the left), upload:
- `newsbot_final.csv` ← from the processed data folder

### 3. Run the Notebooks in Order
```
01 → 02 → 03 → 04 → 05 → 06 → 07
```
> **Shortcut:** Notebook 07 can run standalone — it rebuilds everything from scratch.

### 4. Analyze Any Article
```python
# In Notebook 07
report = analyze_article("Your news article text here...")
print_report(report, "Your news article text here...")
```

---

## 🧠 System Modules

### Notebook 01 — Data Exploration
- Loads and validates the BBC News dataset (1,440 articles)
- Text preprocessing: lowercase → URL removal → tokenization → lemmatization → stopword removal
- Exploratory data analysis with category and sentiment distributions
- **Output:** `newsbot_final.csv`

### Notebook 02 — Advanced Classification ⭐
- Three classifiers: Naive Bayes, Logistic Regression, Linear SVM (Calibrated)
- **97.22% accuracy** with per-class confidence probability scores
- 5-fold cross-validation (97.71% ± 1.11%)
- Feature importance analysis — top predictive words per category
- Error analysis — understanding where and why the model fails

### Notebook 03 — Topic Modeling
- **LDA** (Latent Dirichlet Allocation) — 10 probabilistic topics, perplexity: 1,301.71
- **NMF** (Non-negative Matrix Factorization) — sharper topic boundaries
- Interactive **pyLDAvis** visualization (exported as HTML)
- Topic-to-category heatmap analysis

### Notebook 04 — Language Models
- **Extractive summarization** — 86.4% average compression ratio
- Three algorithms compared: Custom TF-IDF scorer, LSA, LexRank, Luhn (via Sumy)
- **Semantic search engine** — cosine similarity on 10,000-feature TF-IDF space
- Similar article recommendations
- Query expansion for richer search results

### Notebook 05 — Multilingual Intelligence
- **Language detection** across 55+ languages (91%+ accuracy via langdetect)
- **Translation** to English via Google Translate (deep-translator)
- Cross-lingual analysis comparing EN, ES, FR, DE news coverage
- Full multilingual pipeline: detect → translate → analyze

### Notebook 06 — Conversational Interface
- **9 query intents**: search_topic, filter_category, filter_sentiment, count_query, sentiment_stats, top_words_query, compare_categories, summary_query, help
- Plain English queries — no SQL or coding knowledge required
- Multi-turn conversation with history tracking
- Example queries:
  ```
  "Show me positive tech articles"
  "How many politics articles are there?"
  "What are the top words in business?"
  "Compare sentiment across all categories"
  ```

### Notebook 07 — System Integration ⭐
- Unified `analyze_article()` function running all 9 pipeline stages
- Batch processing support (100+ articles)
- 6-panel integration dashboard
- Tests on brand new articles not in training data

---

## 💼 Business Value

| Use Case | Problem Solved | NewsBot Capability |
|----------|---------------|-------------------|
| Media Monitoring | Manually tracking thousands of daily articles | Auto-categorizes at 97.22% accuracy |
| Brand Intelligence | Reading every article for brand mentions | NER extracts entities + sentiment automatically |
| Financial Intelligence | Monitoring market-moving news at scale | Sentiment analysis flags negative signals |
| Global Coverage | Non-English sources inaccessible | Multilingual pipeline handles 55+ languages |
| Stakeholder Reporting | Executives can't query NLP systems | Conversational interface uses plain English |

**ROI Summary (500 articles/day organization):**
- ⏱️ **92% daily time saved** vs manual analysis
- 💰 **$180K+ annual analyst cost avoided**
- 💻 **<$500 annual infrastructure cost** (Google Colab)

---

## 📦 Dataset

| Property | Value |
|----------|-------|
| Name | BBC News Classification Dataset |
| Source | [Kaggle — learn-ai-bbc](https://www.kaggle.com/competitions/learn-ai-bbc/data) |
| Articles | 1,440 |
| Categories | Business, Tech, Politics, Sport, Entertainment |
| Language | English |
| Format | CSV (ArticleId, Text, Category) |

---

## 🛠️ Libraries

```
scikit-learn    — TF-IDF, classification, topic modeling, evaluation
spaCy           — Named entity recognition, dependency parsing
NLTK            — Tokenization, stopwords, lemmatization, POS tagging
pandas          — Data loading and manipulation
numpy           — Numerical operations
matplotlib      — Charts and visualizations
seaborn         — Statistical visualization and heatmaps
sumy            — LSA, LexRank, Luhn summarization algorithms
langdetect      — Language identification (55+ languages)
deep-translator — Google Translate API wrapper
pyLDAvis        — Interactive LDA topic visualization
```

Install all dependencies:
```bash
pip install -r requirements.txt
```

---

## 📈 Classification Performance

| Model | Accuracy | CV Mean | Avg Confidence |
|-------|----------|---------|----------------|
| Naive Bayes | 96.18% | 97.29% ± 1.41% | 87.20% |
| Logistic Regression | 96.88% | 97.57% ± 1.12% | 84.48% |
| **Linear SVM (Calibrated)** | **97.22%** | **97.71% ± 1.11%** | **92.79%** |

**Confidence insight:** Correct predictions averaged **93.75%** confidence vs **59.03%** for incorrect ones — meaning the model's uncertainty reliably predicts its own errors, enabling human-in-the-loop review of low-confidence outputs.

---

## 🌍 Named Entities Extracted

| Entity Type | Total Found | Avg per Article |
|-------------|-------------|-----------------|
| Dates (DATE) | 2,377 | 1.65 |
| People (PERSON) | 2,301 | 1.60 |
| Locations (GPE) | 1,646 | 1.14 |
| Organizations (ORG) | 1,322 | 0.92 |
| Money (MONEY) | 651 | 0.45 |
| **Total** | **8,297** | **5.76** |

---

## 🗺️ Future Roadmap

- **Phase 1 (0-3 months):** Streamlit web interface, BERT-based sentiment, joblib model persistence
- **Phase 2 (3-6 months):** Real-time RSS feed processing, knowledge graph construction, T5 abstractive summarization
- **Phase 3 (6-12 months):** Bias detection module, domain-specific financial classifier
- **Phase 4 (12+ months):** Multimodal analysis, public REST API

---

## 📄 Deliverables

| File | Description |
|------|-------------|
| `FP_TechnicalDoc_YusufShahzad_ITAI2373.docx` | Full system architecture and API reference |
| `FP_ExecutiveSummary_YusufShahzad_ITAI2373.docx` | Business value, ROI, competitive analysis |
| `FP_ReflectiveJournal_YusufShahzad_ITAI2373.pdf` | 3-page individual reflection |
| `FP_Presentation_YusufShahzad_ITAI2373.pptx` | 10-slide presentation deck |

---

## 👤 Author

**Yusuf Shahzad**
ITAI2373 — Natural Language Processing
Final Project — NewsBot Intelligence System 2.0

---

*Built with Python, scikit-learn, spaCy, NLTK, and Google Colab Free Tier*
