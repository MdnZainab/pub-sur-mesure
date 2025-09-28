# Architecture du Système Pub Sur Mesure

## Diagramme du Système
[Caméra] → [Détection Visage] → [Analyse Genre] → [Sélection Pub] → [Affichage]

## Composants Techniques

### 1. Module de Détection Faciale
- **Technologies** : OpenCV, MediaPipe, TensorFlow
- **Fonctions** :
  - Capture vidéo en temps réel
  - Détection des visages
  - Classification homme/femme
- **Performance** : 30 images par seconde

### 2. Gestion des Publicités
- **Organisation** :
  - Dossiers séparés : Homme / Femme
  - Formats supportés : PNG, JPG, GIF
- **Fonctionnalités** :
  - Changement automatique des pubs
  - Vitesse réglable
  - Plein écran

### 3. Interface Utilisateur
- **Framework** : PyQt5
- **Écrans principaux** :
  - Page d'accueil avec connexion
  - Panel administrateur
  - Affichage publicitaire

### 4. Sécurité et Données
- **Authentification** :
  - Inscription avec email
  - Vérification par code
  - Mots de passe cryptés
- **Stockage** :
  - Fichiers JSON pour les utilisateurs
  - Dossiers pour les images
  - Fichiers de configuration

## Fonctionnement

### Processus de Détection
1. La caméra capture une image
2. Le système détecte un visage
3. Analyse si homme ou femme
4. Sélectionne les pubs correspondantes
5. Affiche les pubs à l'écran

### Gestion des Utilisateurs
1. Création de compte avec email
2. Envoi d'un code de vérification
3. Activation du compte
4. Accès à l'application

## Fichiers du Projet
ads/ # Dossier des publicités
├── homme/ # Pubs pour hommes
└── femme/ # Pubs pour femmes

data/ # Données application
├── users.json # Liste des utilisateurs
└── config/ # Fichiers configuration


## Technologies Utilisées

- **Python** : Langage principal
- **OpenCV** : Traitement d'images
- **TensorFlow** : Intelligence artificielle
- **MediaPipe** : Détection faciale
- **PyQt5** : Interface graphique
- **SMTP** : Envoi d'emails