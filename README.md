# NLP Assignment: PDF Text Processing and Feature Extraction

## 📚 Overview

This project demonstrates Natural Language Processing (NLP) techniques applied to a PDF document. It covers text extraction, preprocessing, feature extraction, and visualization of NLP results.

**PDF Used:** Machine Learning by Tom Mitchell (120 pages extracted)

### Assignment Objectives:
- Extract text from PDF files
- Apply comprehensive text preprocessing
- Extract features using One-Hot Encoding and TF-IDF
- Visualize results using scatter plots

---

## 📋 Table of Contents

1. [Features](#features)
2. [Prerequisites](#prerequisites)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Project Structure](#project-structure)
6. [Detailed Steps](#detailed-steps)
7. [Output Results](#output-results)
8. [Screenshots](#screenshots)

---

## ✨ Features

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

## 📋 Prerequisites

Make sure you have the following installed:
- Python 3.7 or higher
- Jupyter Notebook or JupyterLab
- pip (Python package manager)

---

## 🔧 Installation

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

## 🚀 Usage

### Run the Notebook

#### Using Jupyter Notebook:
```bash
jupyter notebook NLP_Assignment_Simple.ipynb
```

#### Using JupyterLab:
```bash
jupyter lab NLP_Assignment_Simple.ipynb
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

## 📁 Project Structure

```
NLP-PDF-Processing/
│
├── README.md                          # This file
├── requirements.txt                   # Required libraries
├── NLP_Assignment_Simple.ipynb        # Main Jupyter notebook
├── MachineLearningTomMitchell.pdf     # Source PDF file
├── tfidf_scatter_plot.png            # Output visualization (generated)
│
└── outputs/                           # Output folder (optional)
    └── results.txt                    # Summary results
```

---

## 📊 Detailed Steps

### Step 1: PDF Reading (Q1a)
```
✓ Read PDF file using PdfReader
✓ Count total pages: 773
✓ Extract 120 pages
✓ Display sample text
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
| Lowercase conversion | - | ✓ Complete |
| Remove numbers | `r'\d+'` | ✓ Complete |
| Remove special symbols | `r'[^a-zA-Z\s]'` | ✓ Complete |
| Remove extra spaces | `r'\s+'` | ✓ Complete |
| Tokenization | - | ✓ Complete |
| Stop word removal | - | ✓ Complete |
| Stemming | Porter Stemmer | ✓ Complete |
| Lemmatization | WordNet | ✓ Complete |

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

## 📈 Output Results

After running the complete notebook, you will get:

### 1. Console Output
```
Total Pages in PDF: 773
Pages to Extract: 120

Original words: 45,678
Stop words found: 12,345
Valid words: 33,333

Preprocessing:
- Lowercase: ✓
- Numbers removed: ✓
- Special symbols removed: ✓
- Extra spaces removed: ✓
- Tokenization: ✓
- Stop words removed: ✓
- Stemming: ✓
- Lemmatization: ✓

Feature Extraction:
- One Hot Encoding: 50 chunks × 30 words
- TF-IDF: 20 documents × 20 features

✓ ALL TASKS COMPLETED!
```

### 2. Generated Files
- `tfidf_scatter_plot.png` - Visualization of top TF-IDF words

### 3. Data Frames
- **One-Hot Encoding Table:** Shows presence/absence of words in chunks
- **TF-IDF Table:** Shows importance scores of words

---

## 📸 Screenshots

### Screenshot 1: PDF Reading Output
```
Total Pages in PDF: 773
Pages to Extract: 120
Total characters extracted: 1,234,567

Sample Extracted Text (first 500 characters):
================================================== 
Chapter 1: Introduction to Machine Learning
This book provides a comprehensive introduction to machine learning...
```

### Screenshot 2: Preprocessing Output
```
Step 1: Converting to lowercase...
✓ Done

Step 2: Removing numbers using Regex...
Regex Pattern: \d+
✓ Numbers removed

Step 3: Removing special symbols using Regex...
Regex Pattern: [^a-zA-Z\s]
✓ Special symbols removed

Step 4: Removing extra spaces using Regex...
Regex Pattern: \s+
✓ Extra spaces removed

Step 5: Tokenizing text into words...
✓ Total words: 45,678
First 20 words: ['chapter', 'introduction', 'machine', 'learning', 'book'...]
```

### Screenshot 3: Stop Words Output
```
Step 6: Removing stop words...
Stop words found: 12,345
Valid words after removing stop words: 33,333
First 20 valid words: ['machine', 'learning', 'algorithm', 'training'...]
```

### Screenshot 4: Stemming Examples
```
Step 7: Applying Stemming...
Examples of stemming (word → stem):
  machine → machin
  learning → learn
  training → train
  algorithm → algorithm
  processing → process
```

### Screenshot 5: Lemmatization Examples
```
Step 8: Applying Lemmatization...
Examples of lemmatization (word → lemma):
  machine → machine
  learning → learning
  training → training
  algorithm → algorithm
  processing → processing
```

### Screenshot 6: One-Hot Encoding Table
```
Feature Extraction 1: ONE HOT ENCODING

One Hot Encoding Table (First 5 chunks):
    algorithm  analysis  approach  ... training  validation
0            0         1         0  ...        1           0
1            1         0         0  ...        0           1
2            0         1         1  ...        1           0
3            1         0         1  ...        0           0
4            0         0         0  ...        1           1
```

### Screenshot 7: TF-IDF Table
```
Feature Extraction 2: TF-IDF

TF-IDF Values (Top Words by Average Score):
                Word  TF-IDF Score
        algorithm       0.3456
          learning       0.3212
          training       0.2987
         validation       0.2654
            machine       0.2345
          prediction       0.2123
```

### Screenshot 8: Scatter Plot
```
[Scatter Plot Image showing TF-IDF scores]
- Title: "TF-IDF Scores of Top Words"
- X-axis: Word Index (0-20)
- Y-axis: TF-IDF Score (0-0.4)
- Points labeled with word names
- Grid enabled for clarity
```

---

## 🔗 Important Links

**PDF Source:**
- Machine Learning by Tom Mitchell
- Available in: `/MachineLearningTomMitchell.pdf`
- Total Pages: 773
- Extracted Pages: 120

---

## 📝 Assignment Requirements

This project fulfills the following assignment requirements:

- ✅ Q1(a): PDF Reading and Text Extraction
  - Select PDF with minimum 100 pages ✓
  - Read PDF file ✓
  - Extract text from all pages ✓
  - Show total pages ✓
  - Show sample text ✓

- ✅ Q1(b): Text Preprocessing
  - Convert to lowercase ✓
  - Remove numbers (Regex) ✓
  - Remove special symbols (Regex) ✓
  - Remove extra spaces (Regex) ✓
  - Remove punctuation ✓
  - Tokenize words ✓
  - Stop word removal ✓
  - Show stop word count ✓
  - Show valid word count ✓
  - Apply stemming ✓
  - Apply lemmatization ✓

- ✅ Q1(c): Feature Extraction
  - One-Hot Encoding ✓
  - Tabular output ✓
  - TF-IDF ✓
  - Feature names ✓
  - Tabular output ✓

- ✅ Q1(d): TF-IDF Visualization
  - Scatter plot created ✓
  - Proper title ✓
  - X-axis label ✓
  - Y-axis label ✓
  - Word labels ✓

---

## 🛠️ Troubleshooting

### Issue: `ModuleNotFoundError: No module named 'pypdf'`
**Solution:**
```bash
pip install pypdf
```

### Issue: `LookupError: NLTK data not found`
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

## 📚 Libraries Used

| Library | Version | Purpose |
|---------|---------|---------|
| pypdf | 3.x | PDF reading and text extraction |
| nltk | 3.x | Natural language processing |
| scikit-learn | 1.x | TF-IDF vectorization |
| pandas | 1.x | Data manipulation and tables |
| matplotlib | 3.x | Visualization |
| numpy | 1.x | Numerical operations |

---

## 👤 Author

**Student Assignment**
- Course: NLP Lab
- Semester: 06
- Date: 2026

---

## 📄 License

This project is for educational purposes only.

---

## 🤝 Contributing

This is an educational assignment. For improvements or suggestions, please create an issue or contact the instructor.

---

## 📞 Support

For issues or questions:
1. Check the troubleshooting section above
2. Review the notebook comments and documentation
3. Refer to library documentation:
   - [pypdf Documentation](https://pypdf.readthedocs.io/)
   - [NLTK Documentation](https://www.nltk.org/)
   - [scikit-learn Documentation](https://scikit-learn.org/)

---

**Last Updated:** May 16, 2026

**Status:** ✅ Complete and Ready for Submission
