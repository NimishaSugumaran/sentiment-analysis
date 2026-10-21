🧠 Sentiment Analysis Web App
A Flask-based web application that analyzes user-submitted reviews using multiple NLP techniques such as sentiment analysis (VADER, RoBERTa, multilingual BERT), keyword extraction (KeyBERT), summarization (DistilBART), toxicity detection (Toxic-BERT), and language translation (MarianMT). The app also stores all analysis data in MongoDB and offers an admin dashboard to view past submissions.

🚀 Features
✅ VADER-based Sentiment Scoring

🤖 RoBERTa-based Transformer Sentiment

🌐 Multilingual Sentiment (supports reviews in Tamil and other languages)

🧠 Keyword Extraction using KeyBERT

📝 Summarization of long reviews

☣️ Toxicity Detection using Toxic-BERT

🌍 Language Detection + Translation to English (via MarianMT)

📦 MongoDB Integration

🧑‍💻 Admin Panel to View Submissions





| Task                   | Model                                              | Source      |
| ---------------------- | -------------------------------------------------- | ----------- |
| VADER Sentiment        | `nltk.sentiment.SentimentIntensityAnalyzer`        | NLTK        |
| Transformer Sentiment  | `cardiffnlp/twitter-roberta-base-sentiment`        | HuggingFace |
| Keyword Extraction     | `KeyBERT`                                          | KeyBERT     |
| Summarization          | `sshleifer/distilbart-cnn-12-6`                    | HuggingFace |
| Toxicity Detection     | `unitary/toxic-bert`                               | HuggingFace |
| Multilingual Sentiment | `nlptown/bert-base-multilingual-uncased-sentiment` | HuggingFace |
| Translation            | `Helsinki-NLP/opus-mt-{lang}-en`                   | HuggingFace |






📁 project-root/
├── app.py               # Main Flask app
├── templates/
│   └── main.html        # HTML template
├── static/              # Optional CSS/JS
├── requirements.txt     # Dependencies
└── README.md            # This file














🔄 Workflow Summary
User submits review (in English or another language).

Language Detection: Determines if review is in English or another language (like Tamil).

Translation (if needed): Uses MarianMT to translate non-English text.

Sentiment Analysis:

VADER for rule-based scoring

RoBERTa for transformer-based sentiment

Multilingual BERT for multilingual sentiment

Keyword Extraction: KeyBERT extracts top keywords.

Summarization: Long reviews are summarized.

Toxicity Detection: Checked for harmful or abusive language.

MongoDB Storage: All data is stored with timestamps.

Admin Panel: Allows viewing of all analysis records.
