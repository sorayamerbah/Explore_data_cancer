# Exploration_data_cancers
exploration statistique descriptive d'un dataset représentant un effectif de patients pris en charge pour un cancer en région Ile de France à l'aide de la bibliothèque ydata_profiling 
1ère Etape: A l'aide de la bibliothèque requests, connexion à l'API de l'assurance maladie qui permet de se connecter à une base de données qui présente des informations sur les effectifs de patients pris en charge par lassurance maladie. pathologie, traitement chronique ou épisode de soins, sexe, classe d’âge, région et département.
Utilisation des requettes where et limitt pour ne récupérer que les patients atteints de cancers, en ilde de frances et se limiter au 100 premières lignes.
récupérations des données dans un dataframe grace à la bibiothèque pandas.


2ème Etape: importation des données dans un une base duckdb, dans un premier temps, la base ameli_cancer est créée puis la table cancers_idf est inserée.
vérification de la table en affichant les 5 premières lignes et suppresion de la colonne "tri" qui n'a aucun interet pour l'analyse statistique.

3ème Etape: la bibliothèque ydata_profiling et la classe ProfileReport ont permis de générer un rapport d'analyse statistique interactive qui permet d'estimer la moyenne, ecart type, min/max, qui pemet de detecter les valeurs manquantes, valeurs abbérantes, donner le type de variable: catégorielle/ quantitative

