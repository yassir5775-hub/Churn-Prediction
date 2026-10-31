# Churn-PredictionPrédiction du Churn Client
Bienvenue dans l'application de prédiction du churn client ! Ce projet utilise des techniques de data science et de machine learning pour analyser les données clients et prédire les risques de churn (désabonnement). L'objectif est de fournir une analyse approfondie pour identifier les clients à risque et permettre aux entreprises de mettre en place des stratégies de rétention efficaces.

📚 Table des Matières
📖 Contexte
🎯 Objectifs
✨ Fonctionnalités
📘 Documentation Complète
🏗️ Structure du Dépôt
🧠 Mise en Place du Modèle Prédictif
⚙️ Installation
🚀 Utilisation
🐳 Docker
👤 Auteur
📖 Contexte
Le churn client, ou attrition client, représente un enjeu majeur pour les entreprises en termes de fidélisation. Comprendre pourquoi les clients se désabonnent est crucial pour optimiser la satisfaction client et minimiser les pertes financières.

🎯 Objectifs
L'application a pour objectifs de :

Analyser les données clients pour identifier les facteurs contribuant au churn.
Prédire les clients à risque grâce à des modèles de machine learning performants.
Fournir des visualisations interactives pour explorer les données et les résultats prédictifs.
Proposer des prédictions individuelles et en lot pour couvrir différents besoins.
📘 Documentation Complète
Une documentation exhaustive est disponible dans le dossier docs/ pour vous aider à maîtriser tous les aspects du projet :

📚 Guides Disponibles
Fondamentaux du Machine Learning

Concepts de base du ML
Types d'apprentissage
Workflow typique
Bonnes pratiques
Types de Tâches en ML

Régression, Classification
Clustering, Détection d'anomalies
Séries temporelles
Comment choisir la bonne approche
Guide Complet des Métriques

Métriques de régression et classification
Quand utiliser quelle métrique
Combiner plusieurs métriques
Métriques business vs ML
Guide Churn Prediction

Qu'est-ce que le churn ?
Impact business et ROI
Création d'un modèle de prédiction
Stratégies de rétention
Meilleures Pratiques EDA

Analyse exploratoire des données
Visualisations recommandées
Feature engineering
Checklist complète
Déploiement et Recommandations

Du notebook à la production
Création d'une API
Docker et CI/CD
Monitoring en production
💡 Conseil : Consultez le README de la documentation pour un guide complet !

✨ Fonctionnalités
1. Dashboard Exploratoire 📊
Visualisation des données brutes et statistiques descriptives.
Graphiques interactifs pour analyser les distributions et les relations avec le churn.
Comparaison des services et des caractéristiques clients.
2. Prédiction Individuelle 🔍
Interface permettant d'entrer les informations d'un client spécifique.
Prédiction du risque de churn avec explication.
3. Prédictions en Lot 🧮
Génération de clients fictifs.
Prédiction du churn pour un grand nombre de clients en une seule opération.
Visualisation des résultats sous forme de graphiques interactifs.
4. Page À Propos 👤
Présentation de l'auteur et contact.
🏗️ Structure du Dépôt
Le projet est organisé comme suit :

Churn-Prediction-and-Analysis-Project/
│
├── data/
│   └── data.csv                # Données utilisées pour le projet
│
├── docs/                       # 📚 Documentation complète
│   ├── 01_machine_learning_fundamentals.md
│   ├── 02_ml_task_types.md
│   ├── 03_metrics_guide.md
│   ├── 04_churn_prediction_guide.md
│   ├── 05_eda_best_practices.md
│   ├── 06_model_deployment_recommendations.md
│   └── README.md
│
├── notebooks/
│   └── Train-Models.ipynb      # Jupyter Notebook pour l'entraînement des modèles
│
├── src/
│   ├── 🏚️Acceuil.py           # Application Streamlit principale (page d'accueil)
│   ├── pages/
│   │   ├── 1_📊_Dashboard_Exploratoire.py
│   │   ├── 2_🔍_Prédiction_Individuelle.py
│   │   ├── 3_🧮_Prédictions_en_Lot.py
│   │   └── 4_👤_À_Propos.py
│   └── models/
│       └── model_LogisticRegression.pkl  # Modèle entraîné
│
├── Dockerfile                  # 🐳 Configuration Docker
├── .dockerignore
├── requirements.txt
└── README.md
🧠 Mise en Place du Modèle Prédictif
La mise en place du modèle prédictif a été réalisée de la manière suivante :

1. Chargement des Données
Les données clients ont été chargées à partir du fichier data/data.csv. Elles contiennent des informations telles que :

Identifiant du client, genre, ancienneté, services souscrits, méthode de paiement, frais mensuels, etc.
Churn (cible) indiquant si le client a quitté l'entreprise.
2. Prétraitement des Données
Nettoyage des Données : Gestion des valeurs manquantes et conversion des types de données.
Encodage des Variables Catégorielles : Utilisation de techniques d'encodage adaptées (Label Encoding et One-Hot Encoding).
Normalisation des Données : Normalisation des variables numériques pour améliorer la performance du modèle.
3. Analyse Exploratoire (EDA)
Analyse Univariée et Bivariée pour comprendre la distribution des variables et leur relation avec le churn.
Visualisations pour identifier les tendances et les schémas pertinents.
4. Création et Entraînement du Modèle
Modèles Testés :
Régression Logistique
Random Forest
SVM (Support Vector Machine)
Pipeline Scikit-learn : Mise en place d'un pipeline comprenant le prétraitement et l'entraînement du modèle.
Validation Croisée : Utilisation de la validation croisée pour évaluer les performances du modèle.
5. Évaluation du Modèle
Métriques Utilisées :
Précision
Rappel
F1-Score
AUC-ROC
Meilleur Modèle : Le modèle final sélectionné est une régression logistique, sauvegardée sous src/models/model_LogisticRegression.pkl.
Pour plus de détails, consultez le notebook notebooks/Model_Building.ipynb.

⚙️ Installation
Prérequis
Python 3.7+ installé.
Pip pour gérer les packages Python.
Étapes d'Installation
Clonez le projet :

git clone https://github.com/yassir5775-hub/Churn-Prediction-and-Analysis-Project.git 
cd Churn-Prediction-and-Analysis-Project
Créez un environnement virtuel :

python -m venv env
Activez l'environnement virtuel :

Sur Windows :

.\env\Scripts\activate
Sur MacOS/Linux :

source env/bin/activate
Installez les dépendances :

pip install -r requirements.txt
🚀 Utilisation
Lancez l'application Streamlit :

streamlit run src/Acceuil.py
Naviguez à travers l'application :

Utilisez la barre latérale pour accéder aux différentes pages.
Explorez les visualisations, effectuez des prédictions individuelles ou en lot.
🐳 Docker
L'application peut être facilement déployée avec Docker pour une portabilité maximale.

Utilisation avec Docker
Construire l'image Docker :

docker build -t churn-prediction-app .
Lancer le conteneur :

docker run -p 8501:8501 churn-prediction-app
Accéder à l'application :

Ouvrez votre navigateur à l'adresse : http://localhost:8501

Utilisation avec Docker Compose (Optionnel)
docker-compose up
CI/CD
Le projet inclut une configuration GitHub Actions pour :

✅ Vérifier que le build Docker fonctionne
✅ Tester l'application automatiquement
✅ Assurer la qualité du code
Consultez .github/workflows/ pour plus de détails.

👤 Auteur
Yassir El Haj Tirari
Data Scientist 
Passionné par les sciences de données et l'intelligence artificielle.
Email : abklb27@gmail.com
💬 Remarques
Pour toute suggestion ou question, veuillez ouvrir un issue sur le dépôt GitHub.

🎉 Merci d'utiliser l'application de prédiction du churn client ! N'oubliez pas de laisser une étoile ⭐ sur le dépôt si vous avez trouvé le projet utile.
