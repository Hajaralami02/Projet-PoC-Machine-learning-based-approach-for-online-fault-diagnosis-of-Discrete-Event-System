# Projet-PoC-Machine-learning-based-approach-for-online-fault-diagnosis-of-Discrete-Event-System

##  Présentation générale du projet

Ce projet a pour objectif de **détecter automatiquement des pannes dans un système industriel** à partir de données temporelles issues de capteurs.  
Il s’agit d’un problème de **classification multi-classes**, où chaque séquence de données correspond à un état du système (fonctionnement normal ou type de panne).

La solution repose sur :
- La **génération de données** simulant différents scénarios industriels.
- L’utilisation d’un **réseau de neurones récurrent (LSTM)** capable d’apprendre des dépendances temporelles.
- L’évaluation du modèle à l’aide de métriques de performance classiques (accuracy, matrice de confusion, etc.).

---

## Organisation du projet

Le projet est divisé en **deux parties principales** :

### Code 1 — Génération des données (Simulation)
Ce module crée un jeu de données artificiel représentant différents comportements du système.

###  Code 2 — Apprentissage automatique
Ce module charge les données générées, entraîne un modèle LSTM et évalue ses performances.


## 🧠 Code 1 : Génération des données simulées

### 🎯 Objectif
Créer un jeu de données réaliste représentant :
- un fonctionnement normal du système,
- plusieurs types de pannes industrielles.


## Code 2 : Apprentissage automatique (LSTM)

### Objectif
Apprendre automatiquement à reconnaître les différents types de pannes à partir des données générées.

### Étapes principales

1. **Chargement des données**
   - Lecture du fichier Excel
   - Séparation des variables d’entrée (X) et de la cible (y)

2. **Prétraitement**
   - Normalisation des données (StandardScaler)
   - Création de séquences temporelles (fenêtre glissante)
   - Encodage one-hot des classes

3. **Création du modèle LSTM**
   - Réseau composé de plusieurs couches LSTM
   - Activation `softmax` pour la classification multi-classes

4. **Entraînement**
   - Optimiseur : Adam  
   - Fonction de perte : categorical_crossentropy  
   - Early stopping pour éviter le surapprentissage

5. **Évaluation**
   - Courbes d’apprentissage (loss & accuracy)
   - Matrice de confusion
   - Analyse des performances par classe

## 📊 Résultats et interprétation

- Le modèle apprend efficacement les patterns temporels.
- Les courbes montrent une bonne convergence.
- La majorité des classes sont correctement reconnues.
- Les erreurs restantes concernent surtout des cas très similaires entre certaines pannes.

## Conclusion

Ce projet démontre qu’un modèle LSTM est **adapté à la détection de pannes**.  
La méthodologie peut être étendue à des données réelles issues de capteurs industriels.

## Perspectives d’amélioration
- Utilisation de données réelles industrielles
- Ajout de nouvelles classes de défauts
- Optimisation des hyperparamètres
- Test d’autres architectures (GRU, Transformer)

📌 **Auteur :** *HAJAR EL ALAMI*  
📅 **Année :** 2025 
📚 **Domaine :** Intelligence Artificielle / Maintenance Prédictive  
