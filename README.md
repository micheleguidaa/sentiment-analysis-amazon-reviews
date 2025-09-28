# Sentiment Analysis Amazon Reviews 📊

A complete project for sentiment analysis on Amazon reviews that compares multiple machine-learning approaches—from traditional to generative—for both binary (2 classes) and multi-class (3 classes) classification.

## 🎯 Goal

This project explores and compares the effectiveness of different approaches to sentiment analysis on Amazon reviews:

* **Rule-based**: VADER Sentiment Analyzer
* **Traditional ML**: TF-IDF + Logistic Regression
* **Generative models**: Google Gemini 2.5-flash-lite

## 📁 Project Structure

```
sentiment-analysis-amazon-reviews/
├── README.md
├── requirements.txt
├── notebooks/                          # Main Jupyter notebooks
│   ├── sa_amazon_reviews_2class.ipynb     # Binary classification (NEG/POS)
│   ├── sa_amazon_reviews_3class.ipynb     # 3-class classification (NEG/NEU/POS)
│  
├── analysis/                           # In-depth analysis notebooks
│   ├── sa_analysis_2class.ipynb
│   └── sa_analysis_3class.ipynb
└── results/                            # Results and predictions
    ├── 2class/
    │   └── predictions/
    │       └── all_predictions.csv
    └── 3class/
        ├── analysis_summary.json      # Metrics summary
        └── predictions/
            └── all_predictions.csv
```

## 🚀 Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/micheleguidaa/sentiment-analysis-amazon-reviews.git
cd sentiment-analysis-amazon-reviews
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure Gemini API (optional)

To use the Gemini model, create a `.env` file in the project root:

```bash
GEMINI_API_KEY=your_api_key_here
```

### 4. Run the notebooks

Open one of the main notebooks:

* `notebooks/sa_amazon_reviews_2class.ipynb` for binary classification
* `notebooks/sa_amazon_reviews_3class.ipynb` for 3-class classification

## 📊 Dataset

The project uses the **Amazon Polarity** dataset from Hugging Face (`mteb/amazon_polarity`):

* **Training set**: 10% of the original dataset (~360K reviews)
* **Test set**: 5% of the original dataset (~20K reviews)
* **Classes**:

  * **2-class**: Negative (0), Positive (1)
  * **3-class**: Negative (0), Neutral (1), Positive (2)

## 🔧 Implemented Models

### 1. VADER (Valence Aware Dictionary and sEntiment Reasoner)

* Rule-based approach
* No training required
* Fast but less accurate

### 2. TF-IDF + Logistic Regression

* Traditional ML approach
* TF-IDF vectorization of reviews
* Classification with Logistic Regression

### 3. Google Gemini

* Advanced generative model
* Contextual text analysis
* Requires API key

## 📈 Results

### 3-Class Classification (Best Performers)

| Model      | Accuracy   | Precision  | Recall     | F1-Score   |
| ---------- | ---------- | ---------- | ---------- | ---------- |
| **TF-IDF** | **75.64%** | **77.08%** | **75.64%** | **76.24%** |
| Gemini     | 73.44%     | 76.07%     | 73.44%     | 73.70%     |
| VADER      | 58.92%     | 56.43%     | 58.92%     | 55.33%     |

### Binary Classification

Results for binary classification generally show higher performance across all models, with accuracy typically above 80%.

## 🛠️ Tech Stack

### Core Libraries

* **pandas**: Data manipulation
* **numpy**: Numerical computing
* **scikit-learn**: Traditional machine learning
* **nltk**: Natural Language Processing
* **Datasets**: Dataset handling

### Visualization

* **matplotlib**: Plotting
* **seaborn**: Statistical visualizations
* **wordcloud**: Word clouds

### APIs & Services

* **google-generativeai**: Gemini integration
* **python-dotenv**: Environment variables

## 📋 Features

* ✅ **Advanced preprocessing**: Text cleaning, tokenization
* ✅ **Multi-model comparison**: 3 different approaches
* ✅ **Comprehensive metrics**: Accuracy, Precision, Recall, F1-Score
* ✅ **Visualizations**: Charts, confusion matrix, word clouds
* ✅ **Results export**: CSV and JSON for further analysis
* ✅ **Interactive notebooks**: Step-by-step analysis
* ✅ **Flexible configuration**: Tunable parameters

## 🔍 In-Depth Analyses

The notebooks in the `analysis/` folder include:

* Exploratory Data Analysis (EDA)
* Class distribution
* Model error analysis
* Detailed performance comparisons
* Advanced visualizations

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Open a Pull Request

## 👨‍💻 Authors

* GitHub: [@micheleguidaa](https://github.com/micheleguidaa)
* GitHub: [@AlessandroSchmitt](https://github.com/AlessandroSchmitt)


---

⭐ If this project was helpful, please leave a star!
