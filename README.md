
---

## 🔍 **Project Description**

This project performs **web article extraction** followed by a **sentiment and readability analysis** using NLP techniques. It is divided into two phases:

---

### **Phase 1: Data Extraction**

* **Purpose:** Extracts the full textual content from given URLs.
* **Input:** `Input.xlsx` file containing `URL_ID` and `URL`.
* **Output:** Plain `.txt` files of each article stored under the `articles/` directory.
* **Key tools used:** `requests`, `BeautifulSoup`, `pandas`.

---

### **Phase 2: Text Cleaning + NLP-Based Analysis**

* **Purpose:** Performs text cleaning, sentiment scoring, readability calculation, word statistics, and pronoun usage.
* **Input:** Text files in the `articles/` directory.
* **Output:**

  * Cleaned versions of articles in `cleaned_texts/`
  * Final results in `text_output_metrics_cumulative.csv`
* **Key NLP features computed:**

  * Sentiment Scores: Positive, Negative, Polarity, Subjectivity
  * Readability: Avg Sentence Length, Complex Word %, Gunning Fog Index
  * Other metrics: Word Count, Syllables/Word, Personal Pronouns, Avg Word Length
* **Key tools used:** `NLTK`, `pandas`, `os`, `re`

---

## ✅ `README.md` File

```markdown
# Article Sentiment and Readability Analyzer

## Overview

This project automates the process of extracting web articles and performing sentiment and readability analysis using Natural Language Processing (NLP).

It consists of two major components:
1. **Data Extraction** – Scrape article content from URLs.
2. **Data Analysis** – Clean text and generate sentiment, readability, and linguistic metrics.

---

## 📁 Directory Structure

```

.
├── Input.xlsx                       # Input file with URL and URL\_ID
├── articles/                       # Stores raw extracted article text
├── cleaned\_texts/                  # Stores cleaned article text
├── text\_output\_metrics\_cumulative.csv   # Final output metrics
├── data\_extraction.py             # Script for Phase 1
├── data\_analysis.py               # Script for Phase 2

````

---

## 🔧 Requirements

Install the necessary packages:
```bash
pip install pandas requests beautifulsoup4 nltk scikit-learn
````

Download required NLTK resources:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

---

## 🚀 How to Run

### Step 1: Extract Articles

```bash
python data_extraction.py
```

* Reads URLs from `Input.xlsx`
* Saves `.txt` files to `articles/`

---

### Step 2: Analyze Extracted Texts

```bash
python data_analysis.py
```

* Cleans the text
* Computes metrics like:

  * Sentiment scores
  * Readability (Fog Index)
  * Word stats
* Saves output to `text_output_metrics_cumulative.csv`

---

## 📊 Output Metrics Include

| Metric                  | Description                             |
| ----------------------- | --------------------------------------- |
| Positive/Negative Score | Based on predefined word lists          |
| Polarity/Subjectivity   | Sentiment strength and objectivity      |
| Fog Index               | Readability metric                      |
| Avg Sentence Length     | Total words / Total sentences           |
| Complex Word Count      | Words with more than 2 syllables        |
| Syllables per Word      | Total syllables / Total words           |
| Personal Pronouns Count | Counts words like *I, we, my, us, ours* |
| Avg Word Length         | Total characters / Total words          |

---

## 📁 Notes

* Make sure `positive-words.txt`, `negative-words.txt`, and all stopword files exist in:

  * `Master_Dictionary/`
  * `stopwords/`

---

## 👨‍💻 Author

Abdul Jabbar
B.Tech in CSE - AI & ML Specialization

```

---

Would you like me to:
- Create a `.zip` with proper folder structure and this README?
- Help convert this into a Streamlit or Flask app?
- Write unit tests for this code?

Let me know.
```
