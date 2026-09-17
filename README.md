![IMDB Sentiment Classification](assets/banner.svg)

[English](README.md) · [Português](README.pt-BR.md) · [Notebook](notebooks/imdb_sentiment_classification.ipynb) · [Portfolio](https://github.com/joaovspereira)

# IMDB Sentiment Classification

> **F1 0.88 · ROC-AUC 0.95**

**Decision question:** Can movie reviews be classified by sentiment with a test F1 of at least 0.85?

**Key result:** The selected TF-IDF + Logistic Regression pipeline exceeds the F1 target.

NLP project for automated classification of movie reviews.

## Business problem
Film Junky Union needs to identify negative reviews automatically.

## Objective
Build a text classifier with **F1 ≥ 0.85** on the test set and compare performance against computational complexity.

## Results
- **Selected pipeline:** NLTK normalization + TF-IDF + Logistic Regression
- **Test F1:** 0.88
- **Test ROC-AUC:** 0.95
- spaCy + TF-IDF + Logistic Regression also reached F1 = 0.88
- spaCy + TF-IDF + LightGBM reached F1 = 0.87

BERT code is retained as an optional experiment (`RUN_BERT = False`). The original GPU attempt failed and produced no validated BERT metric; it is excluded from the comparison.

## Technologies
Python · pandas · scikit-learn · NLTK · spaCy · LightGBM · Transformers/BERT · Matplotlib · Seaborn

## Repository structure
- [notebooks/imdb_sentiment_classification.ipynb](notebooks/imdb_sentiment_classification.ipynb)
- [data/README.md](data/README.md)
- [requirements.txt](requirements.txt)


## Next steps
Threshold tuning, explainability, modern transformer fine-tuning and deployment as an inference service.

## Run locally

Clone the repository, enter its directory and create an environment:

```bash
git clone https://github.com/joaovspereira/imdb-sentiment-classification.git
cd imdb-sentiment-classification
python -m venv .venv
```

Activate it with `source .venv/bin/activate` on macOS/Linux or `.\.venv\Scripts\Activate.ps1` in Windows PowerShell. Then run:

```bash
python -m pip install -r requirements.txt
python -m nltk.downloader stopwords
python -m spacy download en_core_web_sm
python -m notebook notebooks/imdb_sentiment_classification.ipynb
```

Place the original datasets listed in [data/README.md](data/README.md) inside `data/` before executing cells. Dataset files are excluded from version control.

## Reproduction status

TF-IDF metrics are preserved from the original saved run. Publication review fixed dataset paths, missing NLTK setup, obsolete plotting calls and an undefined-model draft cell. The complete training workflow was not rerun during publication. Original dependency versions were not recorded, so requirements are an installation list rather than an exact historical environment lock. The same test set was used for model comparison; future selection and threshold tuning need a separate validation set.

The publication review checked notebook structure and code syntax, but did not rerun the full training process or establish exact environment reproducibility.

## Learning

This project was developed during the TripleTen Data Science bootcamp. It demonstrates a documented analytical workflow, explicit evaluation criteria and interpretation of model limitations.

## Key learning

A compact text pipeline can provide a useful quality–complexity trade-off; transformer experiments need their own validated evidence.

[Explore the complete portfolio](https://github.com/joaovspereira) · [Contact](mailto:joaovitorsouza20pereira@gmail.com)
