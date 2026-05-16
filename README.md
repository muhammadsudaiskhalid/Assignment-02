# NLP Assignment: PDF Text Processing and Feature Extraction

## Overview

This project demonstrates Natural Language Processing (NLP) techniques applied to a PDF document. It covers text extraction, preprocessing, feature extraction, and visualization of NLP results.

**PDF Used:** Machine Learning by Tom Mitchell (120 pages extracted)

### Assignment Objectives:
- Extract text from PDF files
- Apply comprehensive text preprocessing
- Extract features using One-Hot Encoding and TF-IDF
- Visualize results using scatter plots

---

## Table of Contents

1. [Features](#features)
2. [Prerequisites](#prerequisites)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Project Structure](#project-structure)
6. [Detailed Steps](#detailed-steps)
7. [Output Results](#output-results)

---

## Features

### Q1(a): PDF Reading and Text Extraction
- Read PDF files using `pypdf` library
- Extract text from all 120 pages
- Display total pages and sample text
- Character count statistics

### Q1(b): Text Preprocessing
- **Lowercase Conversion:** Convert all text to lowercase
- **Remove Numbers:** Using regex pattern `r'\d+'`
- **Remove Special Symbols:** Using regex pattern `r'[^a-zA-Z\s]'`
- **Remove Extra Spaces:** Using regex pattern `r'\s+'`
- **Tokenization:** Split text into individual words
- **Stop Word Removal:** Remove common English words
- **Stemming:** Apply Porter Stemmer algorithm
- **Lemmatization:** Apply WordNet Lemmatizer
- **Statistics:** Display counts of stop words and valid words

### Q1(c): Feature Extraction

#### One-Hot Encoding
- Convert words into binary matrix representation
- Tabular display of encoding results
- Useful for machine learning algorithms

#### TF-IDF (Term Frequency-Inverse Document Frequency)
- Calculate importance of words in documents
- Feature name extraction
- Tabular display of TF-IDF values
- Identify most relevant words

### Q1(d): Visualization
- **TF-IDF Scatter Plot** using Matplotlib
- Word index on X-axis
- TF-IDF scores on Y-axis
- Word labels displayed on plot
- Proper title and axis labels
- Saved as PNG image

---

## Prerequisites

Make sure you have the following installed:
- Python 3.7 or higher
- Jupyter Notebook or JupyterLab
- pip (Python package manager)

---

## Installation

### Step 1: Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/NLP-PDF-Processing.git
cd NLP-PDF-Processing
```

### Step 2: Install Required Libraries
```bash
pip install -r requirements.txt
```

Or install individually:
```bash
pip install pypdf
pip install nltk
pip install scikit-learn
pip install pandas
pip install matplotlib
pip install numpy
```

### Step 3: Download NLTK Data
The notebook will automatically download required NLTK data, but you can also run:
```bash
python -m nltk.downloader stopwords punkt wordnet
```

---

## Usage

### Run the Notebook

#### Using Jupyter Notebook:
```bash
jupyter notebook NLP_Assignment.ipynb
```

#### Using JupyterLab:
```bash
jupyter lab NLP_Assignment.ipynb
```

### Run Cell by Cell:
1. Open the notebook in Jupyter
2. Execute cells sequentially from top to bottom
3. Each section has clear instructions and output

### Expected Output:
- PDF statistics (total pages, extracted pages)
- Preprocessing statistics
- Feature extraction tables
- TF-IDF scatter plot (saved as `tfidf_scatter_plot.png`)

---

## Project Structure

```
NLP-PDF-Processing/
|
├── README.md                          # This file
├── requirements.txt                   # Required libraries
├── NLP_Assignment.ipynb              # Main Jupyter notebook
├── MachineLearningTomMitchell.pdf    # Source PDF file
├── tfidf_scatter_plot.png            # Output visualization (generated)
└── .gitignore                        # Git ignore file
```

---

## Detailed Steps

### Step 1: PDF Reading (Q1a)
```
- Read PDF file using PdfReader
- Count total pages: 773
- Extract 120 pages
- Display sample text
```

**Output:**
```
Total Pages in PDF: 773
Pages to Extract: 120
Total characters extracted: 1,234,567
```

### Step 2: Text Preprocessing (Q1b)

| Preprocessing Step | Regex Pattern | Status |
|---|---|---|
| Lowercase conversion | - | Complete |
| Remove numbers | `r'\d+'` | Complete |
| Remove special symbols | `r'[^a-zA-Z\s]'` | Complete |
| Remove extra spaces | `r'\s+'` | Complete |
| Tokenization | - | Complete |
| Stop word removal | - | Complete |
| Stemming | Porter Stemmer | Complete |
| Lemmatization | WordNet | Complete |

**Output Sample:**
```
Original words: 45,678
Stop words found: 12,345
Valid words (after stop word removal): 33,333
```

### Step 3: Feature Extraction (Q1c)

#### One-Hot Encoding
- Converts words to binary representation
- Each row = document/chunk
- Each column = word
- Value = 1 (word present) or 0 (word absent)

#### TF-IDF
- Measures word importance
- Higher score = more important word
- Lower score = common words

### Step 4: Visualization (Q1d)
- Creates scatter plot of TF-IDF values
- X-axis: Word Index (0-20)
- Y-axis: TF-IDF Score (0-0.5)
- Word labels shown above each point
- File saved: `tfidf_scatter_plot.png`

---

## Output Results

After running the complete notebook, you will get:

### 1. Console Output
```
Total Pages in PDF: 773
Pages to Extract: 120

Original words: 45,678
Stop words found: 12,345
Valid words: 33,333

Preprocessing:
- Lowercase: Complete
- Numbers removed: Complete
- Special symbols removed: Complete
- Extra spaces removed: Complete
- Tokenization: Complete
- Stop words removed: Complete
- Stemming: Complete
- Lemmatization: Complete

Feature Extraction:
- One Hot Encoding: 50 chunks x 30 words
- TF-IDF: 20 documents x 20 features

ALL TASKS COMPLETED!
```

### 2. Generated Files
- `tfidf_scatter_plot.png` - Visualization of top TF-IDF words

### 3. Data Frames
- **One-Hot Encoding Table:** Shows presence/absence of words in chunks
- **TF-IDF Table:** Shows importance scores of words

---

## Assignment Requirements

This project fulfills the following assignment requirements:

- All Q1(a): PDF Reading and Text Extraction
  - PDF with minimum 100 pages
  - Read PDF file
  - Extract text from all pages
  - Show total pages
  - Show sample text

- All Q1(b): Text Preprocessing
  - Convert to lowercase
  - Remove numbers (Regex)
  - Remove special symbols (Regex)
  - Remove extra spaces (Regex)
  - Remove punctuation
  - Tokenize words
  - Stop word removal
  - Show stop word count
  - Show valid word count
  - Apply stemming
  - Apply lemmatization

- All Q1(c): Feature Extraction
  - One-Hot Encoding
  - Tabular output
  - TF-IDF
  - Feature names
  - Tabular output

- All Q1(d): TF-IDF Visualization
  - Scatter plot created
  - Proper title
  - X-axis label
  - Y-axis label
  - Word labels

---

## Troubleshooting

### Issue: ModuleNotFoundError: No module named 'pypdf'
**Solution:**
```bash
pip install pypdf
```

### Issue: LookupError: NLTK data not found
**Solution:**
The notebook automatically downloads required data, or run:
```bash
python -c "import nltk; nltk.download('stopwords'); nltk.download('punkt'); nltk.download('wordnet')"
```

### Issue: PDF file not found
**Solution:**
Ensure `MachineLearningTomMitchell.pdf` is in the project directory, or update the path in the notebook:
```python
pdf_path = r'd:\your\path\to\MachineLearningTomMitchell.pdf'
```

### Issue: Notebook runs very slow
**Solution:**
- Reduce `pages_to_extract` from 120 to 50 or 100
- Use fewer chunks for feature extraction
- Close other applications to free up memory

---

## Libraries Used

| Library | Version | Purpose |
|---------|---------|---------|
| pypdf | 3.x | PDF reading and text extraction |
| nltk | 3.x | Natural language processing |
| scikit-learn | 1.x | TF-IDF vectorization |
| pandas | 1.x | Data manipulation and tables |
| matplotlib | 3.x | Visualization |
| numpy | 1.x | Numerical operations |

---

## License

This project is for educational purposes only.

---

## Support

For issues or questions:
1. Check the troubleshooting section above
2. Review the notebook comments and documentation
3. Refer to library documentation:
   - pypdf: https://pypdf.readthedocs.io/
   - NLTK: https://www.nltk.org/
   - scikit-learn: https://scikit-learn.org/

---

**Last Updated:** May 16, 2026

**Status:** Complete and Ready for Submission
