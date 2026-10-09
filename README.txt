Mini-projet NLP : football ou basket-ball ?
===========================================

Classification de courts textes décrivant une action de jeu selon le sport
(football américain ou basket-ball). Trois systèmes sont comparés sur les mêmes
données et le même test : des règles à base de mots-clés, un MLP PyTorch sur
TF-IDF, et DistilBERT pré-entraîné avec une tête de classification.


Contenu
-------
- projet.ipynb : le notebook complet (données, trois systèmes, évaluation).
- rapport.tex  : le rapport (à compiler en PDF, voir plus bas).
- README.txt   : ce fichier.


Dépendances
-----------
Testé avec Python 3.14 et les versions suivantes :

  pandas 3.0, pyarrow 25.0, numpy 2.5, matplotlib 3.11,
  scikit-learn 1.9, torch 2.14 (CPU), transformers 5.19, ipykernel 7.4

Installation (dans un environnement virtuel) :

  pip install pandas pyarrow numpy matplotlib scikit-learn transformers ipykernel
  pip install torch --index-url https://download.pytorch.org/whl/cpu

Aucun GPU n'est nécessaire.


Données
-------
Le jeu de données est téléchargé automatiquement depuis Hugging Face au
lancement du notebook (its-zion-18/sports-text-dataset, version "augmented"),
aucun fichier n'est à fournir. Le modèle distilbert-base-uncased (environ
250 Mo) est lui aussi téléchargé au premier lancement, puis mis en cache.
Une connexion internet est donc nécessaire la première fois.


Exécution
---------
1. Ouvrir projet.ipynb dans Jupyter ou VS Code.
2. Choisir le noyau Python de l'environnement où les dépendances sont installées.
3. Redémarrer le noyau et tout exécuter (Restart + Run All), dans l'ordre.

L'exécution complète prend environ une minute sur CPU (hors téléchargements).
La seed est fixée (SEED = 213) : le découpage et les scores sont reproductibles.
Les temps d'entraînement et d'inférence varient selon la machine.


Compiler le rapport
-------------------
  pdflatex rapport.tex

ou importer rapport.tex dans Overleaf. Seuls des paquets LaTeX standards sont
utilisés.
