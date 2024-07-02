### 🏠 Prédiction des Prix des Maisons

#### 📑 Table des Matières
1. [📖 Description du Projet](#description-du-projet)
2. [🎯 Objectifs](#objectifs)
3. [📊 Acquisition et Traitement des Données](#acquisition-et-traitement-des-données)
4. [🛠 Développement des Modèles](#développement-des-modèles)
5. [🌐 API et Interface](#api-et-interface)
6. [📦 Conteneurisation](#conteneurisation)
7. [🚀 Utilisation](#utilisation)
8. [⚙️ Installation](#installation)
9. [🔗 Liens GitHub et DockerHub](#liens-github-et-dockerhub)
10. [📜 Licence](#licence)
11. [📧 Contact](#contact)

---

#### 📖 Description du Projet
Ce projet consiste à construire un modèle de machine learning pour prédire les prix des maisons en fonction de diverses caractéristiques telles que la localisation, la taille, le nombre de pièces, etc.

#### 🎯 Objectifs
- Construire un modèle de machine learning pour prédire les prix des maisons.
- Traiter les valeurs manquantes et encoder les variables catégorielles.
- Mettre à l'échelle les caractéristiques de manière appropriée.
- Développer et comparer différents modèles de machine learning.
- Fournir une interface conviviale pour les prédictions.

#### 📊 Acquisition et Traitement des Données
- **📥 Lecture des Données**: Les données sont chargées à partir de fichiers CSV.
- **🧹 Traitement des Données**:
  - **📈 Visualisation**: Utilisation de Matplotlib pour visualiser les données.
  - **🧽 Nettoyage**: Traitement des valeurs manquantes et encodage des variables catégorielles avec Pandas.
  - **📏 Méthode des Quartiles**: Utilisée pour supprimer les outliers.

#### 🛠 Développement des Modèles
- **🎓 Entraînement des Modèles**: Utilisation de diverses techniques pour entraîner plusieurs modèles de machine learning.
- **🏆 Sélection des Modèles**: Choix des 3 meilleurs modèles basés sur la métrique RMSE.
- **📉 Visualisation des Performances**: Utilisation de Matplotlib pour visualiser les performances des modèles.
- **🔧 Fine-Tuning**: Affinage des hyperparamètres des modèles sélectionnés et nouvelle comparaison des performances.
- **📁 Finalisation**: Entraînement du modèle final sur l'ensemble des données avec les meilleurs hyperparamètres et sauvegarde du modèle.

#### 🌐 API et Interface
- **⚙️ Création de l'API**: Développement d'une API utilisant FastAPI pour servir le modèle de prédiction.
- **💻 Interface Streamlit**: Développement d'une application Streamlit pour fournir une interface utilisateur interactive.
- **🔗 Endpoints**: L'API inclut un endpoint pour envoyer des requêtes de prédiction et renvoyer les valeurs prédites.

#### 📦 Conteneurisation
- **🛠 Création des Images Docker**:
  - Une image pour l'API FastAPI.
  - Une image pour l'application Streamlit.
- **📤 Déploiement sur Docker Hub**: Les deux images sont déployées sur Docker Hub pour un accès facile.

#### 🚀 Utilisation
- **🔗 Colab Link**: Un notebook Colab contenant toutes les étapes, explications et résultats est fourni.
- **📜 Script de Prédiction**: Un script simple est inclus pour charger le modèle entraîné et faire des prédictions sur de nouvelles données.

#### ⚙️ Installation
Pour installer et exécuter le projet en local, veuillez suivre les étapes ci-dessous :

##### Cloner les Repositories GitHub
1. **Cloner le repository du notebook et des données :**
   ```bash
   git clone https://github.com/abrahamkoloboe27/Housing-Price-Prediction.git
   ```

2. **Cloner le repository de l'API :**
   ```bash
   git clone https://github.com/abrahamkoloboe27/API-Housing-Price-Prediction.git
   cd API-Housing-Price-Prediction
   ```

3. **Installer les dépendances et lancer l'API :**
   ```bash
   pip install -r requirements.txt
   uvicorn api:app --reload
   ```

4. **Cloner le repository de l'application Streamlit :**
   ```bash
   git clone https://github.com/abrahamkoloboe27/App-Streamlit-Housing-Price-Prediction.git
   cd App-Streamlit-Housing-Price-Prediction
   ```

5. **Installer les dépendances et lancer l'application Streamlit :**
   ```bash
   pip install -r requirements.txt
   streamlit run app.py
   ```

##### Utiliser les Conteneurs Docker depuis Docker Hub
1. **Puller et lancer le conteneur Docker de l'API :**
   ```bash
   docker pull zach27/housing-price-prediction:api
   docker run -d -p 8000:8000 zach27/housing-price-prediction:api
   ```

2. **Puller et lancer le conteneur Docker de l'application Streamlit :**
   ```bash
   docker pull zach27/housing-price-prediction:app_streamlit
   docker run -d -p 8501:8501 zach27/housing-price-prediction:app_streamlit
   ```

#### 🔗 Liens GitHub et DockerHub
- [Notebook et données](https://github.com/abrahamkoloboe27/Housing-Price-Prediction)
- [API](https://github.com/abrahamkoloboe27/API-Housing-Price-Prediction)
- [Application Streamlit](https://github.com/abrahamkoloboe27/App-Streamlit-Housing-Price-Prediction)
- [DockerHub](https://hub.docker.com/repository/docker/zach27/housing-price-prediction)

#### 📜 Licence
Ce projet est sous licence MIT. Veuillez vous référer au fichier LICENSE dans le repository GitHub pour plus de détails.

#### 📧 Contact
Pour toute question ou suggestion, veuillez contacter Abraham KOLOBOE à l'adresse email [abklb27@gmail.com](mailto:abklb27@gmail.com).
