# Análise de Sentimento com NLP (IMDb)

Este projeto implementa um pipeline simples de Processamento de Linguagem Natural (NLP) para classificação de reviews de filmes como positivos ou negativos, utilizando o dataset IMDb.

## Objetivo

Comparar diferentes abordagens de representação de texto e modelos de machine learning para análise de sentimento.

## Dataset

Foi utilizado o dataset IMDb, contendo:

- 25.000 reviews para treino
- 25.000 reviews para teste
- 50.000 exemplos não rotulados (não utilizados)

Cada review possui:
- `text`: conteúdo do review
- `label`: 0 (negativo) ou 1 (positivo)

## Pipeline

O projeto segue as seguintes etapas:

1. Carregamento dos dados
2. Vetorização de texto
3. Treinamento de modelos
4. Avaliação

## Vetorização

Foram utilizadas duas abordagens:

- **Bag of Words (BoW)**: representação baseada em contagem de palavras
- **TF-IDF**: pondera palavras com base em sua importância no corpus

## Modelos

Foram treinados dois modelos:

- Regressão Logística
- Naive Bayes (Multinomial)

## Resultados

| Vetorizador | Modelo              | Acurácia |
|------------|----------------------|----------|
| BoW        | Regressão Logística  | 86.32%   |
| BoW        | Naive Bayes          | 81.57%   |
| TF-IDF     | Regressão Logística  | 88.37%   |
| TF-IDF     | Naive Bayes          | 83.22%   |

## Conclusões

- TF-IDF apresentou melhor desempenho que BoW
- Regressão Logística superou Naive Bayes
- A combinação TF-IDF + Regressão Logística foi a melhor

## Licença

Este projeto está disponível sob a licença MIT.
