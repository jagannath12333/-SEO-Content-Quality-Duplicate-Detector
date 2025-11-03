SEO Content Quality and Duplicate Detector
Overview

This project analyzes web pages for SEO quality and duplicate detection using NLP and machine learning techniques.
It evaluates content readability, sentiment, keyword density, and identifies near-duplicate URLs to determine overall content quality.

Features

Parses and cleans HTML content

Computes readability and sentiment metrics

Detects duplicate or similar web pages using cosine similarity

Classifies content as High, Medium, or Low quality

Real-time analysis function to test new URLs

Optional Streamlit web app for deployment

Project Structure
seo-content-detector/
├── data/
│   ├── data.csv
│   ├── extracted_content.csv
│   ├── features.csv
│   └── duplicates.csv
├── notebooks/
│   └── seo_pipeline.ipynb
├── streamlit_app/
│   ├── app.py
│   ├── models/
│   │   ├── quality_model.pkl
│   │   └── scaler.pkl
│   └── utils/
├── requirements.txt
└── README.md

Setup Instructions

Clone the repository:

git clone https://github.com/yourusername/seo-content-detector.git
cd seo-content-detector


Install dependencies:

pip install -r requirements.txt


Run locally:

streamlit run streamlit_app/app.py

Key Decisions

Libraries used: scikit-learn, BeautifulSoup4, TextBlob, TextStat

Similarity threshold for duplicates: 0.8

Model: RandomForestClassifier with GridSearchCV

SMOTE used for class balancing

Features used for training: word count, char count, average word length, sentiment polarity, readability score

Results Summary

Total pages analyzed: 81

Duplicate pairs found: 25

Model Accuracy: 95%

Label distribution: Low (50), Medium (27), High (4)

Top important features:

Word Count

Flesch Reading Ease

Sentiment Polarity

Limitations

Small dataset size may limit generalization

Readability metrics may vary for technical content

No deep contextual embedding (BERT or transformer-based models not used)

Future Improvements

Integrate transformer embeddings for better similarity detection

Add visualization dashboard for content quality trends

Extend duplicate detection to domain-level comparison

Author

Jagannath Iyer
MSc Data Science, 2025
