![IMDB Sentiment Classification](assets/banner.svg)

[English](README.md) · **Português** · [Portfólio](https://github.com/joaovspereira)

# IMDB Sentiment Classification

## Problema e objetivo

Classificar o sentimento de avaliações de filmes e atingir F1 de pelo menos 0,85.

## Resultados documentados

TF-IDF + Regressão Logística: F1 de 0,88 e ROC-AUC de 0,95. LightGBM: F1 de 0,87.

## Método

Normalização de texto, remoção de stopwords, lematização, vetorização TF-IDF e comparação de classificadores.

## Tecnologias

Python · pandas · scikit-learn · NLTK · spaCy · TF-IDF · LightGBM

## Evidências e execução

- [Notebook completo](notebooks/imdb_sentiment_classification.ipynb)
- [Arquivos de dados necessários](data/README.md)
- [Dependências](requirements.txt)
- [Instruções de instalação](README.md#run-locally)

## Escopo e limitações

Métricas preservadas da execução original; o mesmo conjunto de teste foi usado para comparar modelos. BERT é um experimento opcional sem métrica validada. A publicação não reexecutou o treinamento completo. As dependências não representam um ambiente histórico travado por versão.

Projeto educacional desenvolvido no Data Science Bootcamp da TripleTen. A revisão de publicação dos projetos, exceto a reexecução documentada do petróleo, verificou estrutura e sintaxe sem repetir o treinamento completo. Os datasets não são redistribuídos.

[João Vitor Pereira](https://github.com/joaovspereira) · [Contato](mailto:joaovitorsouza20pereira@gmail.com)
