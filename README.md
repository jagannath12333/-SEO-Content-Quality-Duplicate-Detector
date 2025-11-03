SEO Content Quality and Duplicate Detector
Overview

This project analyzes web pages for SEO quality and duplicate detection using NLP and machine learning techniques.
It evaluates content readability, sentiment, and keyword density, and identifies near-duplicate URLs to assess overall content quality.

Features

Parses and cleans raw HTML text

Computes readability and sentiment metrics

Detects near-duplicate content using cosine similarity

Classifies content into High, Medium, or Low quality categories

Real-time URL analysis function for quick evaluation

Project Structure

All files are located in a single folder (no subdirectories):

seo-content-detector/
├── data.csv
├── extracted_content.csv
├── features.csv
├── duplicates.csv
├── seo_pipeline.ipynb
├── quality_model.pkl
├── scaler.pkl
├── requirements.txt
└── README.md

Setup Instructions
1. Clone the repository
git clone https://github.com/jagannath12333/seo-content-detector.git
cd seo-content-detector

2. Install dependencies
pip install -r requirements.txt

3. Run the Notebook

Open the Jupyter Notebook:

seo_pipeline.ipynb


Run all cells to reproduce the full pipeline — including preprocessing, feature extraction, duplicate detection, model training, and evaluation.

Key Decisions

Libraries used: scikit-learn, BeautifulSoup4, TextBlob, TextStat, Imbalanced-learn

Duplicate similarity threshold: 0.8 (cosine similarity)

Classifier used: RandomForestClassifier (optimized using GridSearchCV)

Imbalance handling: SMOTE

Main features: word_count, char_count, avg_word_length, sentiment_polarity, flesch_reading_ease

Results Summary
Metric	Value
Total Pages Analyzed	81
Duplicate Pairs Found	25
Final Model Accuracy	95%
Labels Distribution	Low (50), Medium (27), High (4)

Top 3 Most Important Features

Word Count

Flesch Reading Ease

Sentiment Polarity

Outputs

Full model performance, including classification report, confusion matrix, and feature importance plots, are available inside the GitHub repository.

The trained model (quality_model.pkl) and scaler (scaler.pkl) are included for reproducibility.

Limitations

Dataset is small (81 rows) which limits model generalization.

Readability scores can vary across technical or marketing content.

No transformer-based embeddings (BERT) were used for semantic understanding.

Future Enhancements

Add transformer-based embeddings for advanced text representation.

Extend duplicate detection to multi-domain comparisons.

Automate quality monitoring for new content uploads.

Author

Jagannath Iyer
MSc Data Science, 2025
