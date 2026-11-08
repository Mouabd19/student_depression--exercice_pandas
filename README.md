# Exploration du Student Depression Dataset

## Pourquoi ce projet

L'idée m'est venue en pleine mobilisation étudiante en France, où la santé mentale et les conditions de vie des étudiants reviennent au cœur des discussions. En cherchant des données sur le sujet, je suis tombé sur ce dataset Kaggle consacré à la dépression chez les étudiants, et j'ai voulu voir ce que les chiffres pouvaient en dire.

## Les données

Le dataset décrit 4 464 étudiants, avec 13 variables : profil (genre, âge, milieu familial, situation amoureuse et maritale, mode de vie), scolarité (semestre, moyenne CGPA sur 4), état de santé, coût de la vie hors études, région d'origine, et une variable indiquant si l'étudiant se déclare en dépression (Yes/No).

Les étudiants interrogés viennent du Bangladesh, et non de France : les résultats ne sont donc pas directement transposables à la situation des étudiants français.

Source : [Student Depression Dataset sur Kaggle](LIEN_KAGGLE)

## Objectif

Il s'agit d'une analyse exploratoire, réalisée avec pandas et numpy : comprendre la structure et la qualité des données, puis observer comment le taux de dépression varie selon le profil des étudiants (cercle d'amis, état de santé, résultats scolaires, milieu familial…). Aucun modèle de prédiction n'est entraîné à ce stade.

## Principaux résultats

- 26,9 % des étudiants déclarent être en dépression.
- Les étudiants sans cercle d'amis sont plus souvent en dépression (34,3 % contre 24 %).
- Le milieu familial compte : 30,6 % en « Lower Middle class » contre 17,6 % en « Rich class ».
- L'état de santé est lié de façon presque parfaite à la dépression (0 % pour « Good », 100 % pour « Critical »), ce qui pose des questions sur ce que mesure vraiment cette colonne.

Ce sont des corrélations, pas des liens de cause à effet.

## Contenu du dépôt

```
├── data/
│   └── Student_Depression_Dataset.csv
├── notebooks/
│   └── 01_exploration.ipynb
├── requirements.txt
└── README.md
```

## Lancer le notebook

```bash
pip install -r requirements.txt
jupyter notebook notebooks/01_exploration.ipynb
```
