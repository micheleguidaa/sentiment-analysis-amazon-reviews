# Sentiment Analysis Amazon Reviews 📊

Un progetto completo di sentiment analysis per recensioni Amazon che confronta diversi approcci di machine learning, dal tradizionale al generativo, per classificazioni sia binarie (2 classi) che multi-classe (3 classi).

## 🎯 Obiettivo

Questo progetto esplora e confronta l'efficacia di diversi approcci per l'analisi del sentiment su recensioni Amazon:
- **Rule-based**: VADER Sentiment Analyzer
- **Machine Learning tradizionale**: TF-IDF + Logistic Regression
- **Modelli generativi**: Google Gemini

## 📁 Struttura del Progetto

```
sentiment-analysis-amazon-reviews/
├── README.md
├── requirements.txt
├── notebooks/                          # Notebook Jupyter principali
│   ├── sa_amazon_reviews_2class.ipynb     # Classificazione binaria (NEG/POS)
│   ├── sa_amazon_reviews_3class.ipynb     # Classificazione a 3 classi (NEG/NEU/POS)
│   └── sa_amazon_reviews_2class Alesandro.ipynb
├── analysis/                           # Notebook di analisi approfondita
│   ├── sa_analysis_2class.ipynb
│   └── sa_analysis_3class.ipynb
└── results/                            # Risultati e predizioni
    ├── 2class/
    │   └── predictions/
    │       └── all_predictions.csv
    └── 3class/
        ├── analysis_summary.json      # Riassunto delle metriche
        └── predictions/
            └── all_predictions.csv
```

## 🚀 Quick Start

### 1. Clona il repository
```bash
git clone https://github.com/micheleguidaa/sentiment-analysis-amazon-reviews.git
cd sentiment-analysis-amazon-reviews
```

### 2. Installa le dipendenze
```bash
pip install -r requirements.txt
```

### 3. Configura Gemini API (opzionale)
Per utilizzare il modello Gemini, crea un file `.env` nella root del progetto:
```bash
GEMINI_API_KEY=your_api_key_here
```

### 4. Esegui i notebook
Apri uno dei notebook principali:
- `notebooks/sa_amazon_reviews_2class.ipynb` per classificazione binaria
- `notebooks/sa_amazon_reviews_3class.ipynb` per classificazione a 3 classi

## 📊 Dataset

Il progetto utilizza il dataset **Amazon Polarity** da Hugging Face (`mteb/amazon_polarity`):
- **Training set**: 10% del dataset originale (~360K recensioni)
- **Test set**: 5% del dataset originale (~20K recensioni)
- **Classi**: 
  - **2-class**: Negativo (0), Positivo (1)
  - **3-class**: Negativo (0), Neutro (1), Positivo (2)

## 🔧 Modelli Implementati

### 1. VADER (Valence Aware Dictionary and sEntiment Reasoner)
- Approccio rule-based
- Non richiede training
- Veloce ma meno accurato

### 2. TF-IDF + Logistic Regression
- Approccio ML tradizionale
- Vectorizzazione TF-IDF delle recensioni
- Classificazione con Regressione Logistica

### 3. Google Gemini
- Modello generativo avanzato
- Analisi contestuale del testo
- Richiede API key

## 📈 Risultati

### Classificazione a 3 Classi (Migliori Performance)
| Modello | Accuracy | Precision | Recall | F1-Score |
|---------|----------|-----------|--------|----------|
| **TF-IDF** | **75.64%** | **77.08%** | **75.64%** | **76.24%** |
| Gemini | 73.44% | 76.07% | 73.44% | 73.70% |
| VADER | 58.92% | 56.43% | 58.92% | 55.33% |

### Classificazione Binaria
I risultati per la classificazione binaria mostrano performance generalmente superiori per tutti i modelli, con accuratezza tipicamente superiore all'80%.

## 🛠️ Tecnologie Utilizzate

### Core Libraries
- **pandas**: Manipolazione dati
- **numpy**: Calcoli numerici
- **scikit-learn**: Machine learning tradizionale
- **nltk**: Natural Language Processing

### Deep Learning & Transformers
- **PyTorch**: Framework deep learning
- **Transformers**: Modelli pre-addestrati (Hugging Face)
- **Datasets**: Gestione dataset

### Visualizzazione
- **matplotlib**: Plotting
- **seaborn**: Visualizzazioni statistiche
- **wordcloud**: Nuvole di parole

### API & Servizi
- **google-generativeai**: Integrazione Gemini
- **python-dotenv**: Gestione variabili ambiente

## 📋 Features

- ✅ **Preprocessing avanzato**: Pulizia testi, tokenizzazione
- ✅ **Confronto multi-modello**: 3 approcci diversi
- ✅ **Metriche complete**: Accuracy, Precision, Recall, F1-Score
- ✅ **Visualizzazioni**: Grafici, confusion matrix, word clouds
- ✅ **Export risultati**: CSV e JSON per analisi successive
- ✅ **Notebook interattivi**: Analisi step-by-step
- ✅ **Configurazione flessibile**: Parametri modificabili

## 🔍 Analisi Approfondite

I notebook nella cartella `analysis/` contengono:
- Analisi esplorativa dei dati (EDA)
- Distribuzione delle classi
- Analisi degli errori per modello
- Confronto prestazioni dettagliato
- Visualizzazioni avanzate

## 🚦 Prossimi Sviluppi

- [ ] Implementazione modelli Transformer (BERT, RoBERTa)
- [ ] Ottimizzazione iperparametri automatica
- [ ] Ensemble methods
- [ ] Analisi aspetti specifici (aspect-based sentiment)
- [ ] Deploy come web service

## 🤝 Contributi

I contributi sono benvenuti! Per contribuire:
1. Fork del repository
2. Crea un branch per la tua feature (`git checkout -b feature/nuova-feature`)
3. Commit delle modifiche (`git commit -am 'Aggiunge nuova feature'`)
4. Push al branch (`git push origin feature/nuova-feature`)
5. Apri una Pull Request

## 📄 Licenza

Questo progetto è rilasciato sotto licenza MIT. Vedi il file `LICENSE` per dettagli.

## 👨‍💻 Autore

**Michele Guida**
- GitHub: [@micheleguidaa](https://github.com/micheleguidaa)

---

⭐ Se questo progetto ti è stato utile, lascia una stella!