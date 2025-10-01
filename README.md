# Exploration_data_cancers
Exploration statistique d'un dataset représentant des patients pris en charge par l'assurance maladie pour un cancer en région Ile de France à l'aide de la bibliothèque ydata_profiling 

1ère Etape: A l'aide de la bibliothèque Requests, connexion à l'API d'une base de données de l'assurance maladie qui regroupe des informations sur des effectifs de patients pris en charge par lassurance maladie: type de pathologie, traitement chronique ou épisode de soins, sexe, classe d’âge, région et département.
Utilisation des requettes "where" et "limitt" pour ne récupérer que les patients atteints de cancers, en region ile de france et se limiter aux 100 premières lignes.
récupérations des données dans un dataframe grace à la bibiothèque pandas.


2ème Etape: importation des données dans la base duckdb, dans une table nommée cancers_idf.
vérification de la présence de table en affichant les 5 premières lignes et suppression de la colonne "tri" qui n'a aucun interet pour l'analyse statistique.

3ème Etape: la bibliothèque ydata_profiling permet de réaliser une analyse statistique détaillée, incluant plusieurs type d'analyses:
          * analyse globale du dataset (nombre de variables, pourcentage de doublons, données manquantes)
          * type de variable: catégorique ou numérique
          * estimation des paramètres (moyenne, ecart-type, min/max)
          * analyse univariée et multivariée
          * étude d'interraction entre les variables (étude interractive puisqu'on peut selectionner les variables)
          * étude de corrélation avec le heatmap  

Le rapport est téléchargeable en bas du Notebook data_cancers_IDF

