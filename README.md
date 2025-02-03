# 🌊 Smart Dive Computer (SDC)

## 📌 Description du Projet
Le projet **Smart Dive Computer (SDC)** vise à développer un **ordinateur de plongée intelligent** pour accompagner les plongeurs en leur fournissant des fonctionnalités :  
- Décompression en temps réel  
- Navigation sous-marine  
- Captation vidéo/photo  
- Planification et gestion des plongées  

Ce système est basé sur un **Raspberry Pi Zero** et intègre des **capteurs sous-marins**, une **interface utilisateur avancée**, et des **algorithmes de décompression**.  

---

## 🎯 Objectifs du Projet
✅ Développer un **système embarqué** basé sur un **Raspberry Pi Zero**  
✅ Concevoir une **application en Python** pour la lecture et l’affichage des données des capteurs  
✅ Implémenter des **algorithmes de décompression** (Bühlmann, MN90)  
✅ Assurer la communication entre les composants via **REST API**  
✅ Déployer une **base de données** pour stocker l’historique des plongées et les statistiques  

---

## 📂 Architecture Haut Niveau
L’architecture suit un **modèle composant-connecteur** et inclut les éléments suivants :

### 🏊‍♂️ **Capteurs (Sensors)**
- **Pressure** : Mesure la pression sous-marine  
- **Temperature** : Capture la température de l’eau  
- **Compass** : Orientation du plongeur  
- **GPS** : Position en surface  
- **Air** : Quantité d’air restante  
- **Oceanographic Parameters** : Qualité de l’eau  
- **Camera** : Captation vidéo/photo  

### 🔢 **Calculator**
- Transformation des **données des capteurs** (conversion, agrégation)  
- Implémentation des **algorithmes de décompression**  

### 🖥️ ** HMI **
- **Affichage en temps réel** des données  
- **Configuration des paramètres** de plongée  

### 📊 **Data**
- **Sauvegarde en temps réel** des plongées  

### 📜 **Historian**
- **Stockage et gestion des historiques**  

### 📈 **Management**
- **Analyse et planification des plongées**  
- **Génération de statistiques et alertes**  

---

## 🛠️ Technologies et Contraintes Techniques
**🖥️ Matériel**  
- Raspberry Pi Zero (OS : Raspbian)  

**📝 Langages de programmation**  
- Python (calculateur et backend)  
- HTML / CSS / JavaScript (interface utilisateur)  

**📡 Communication**  
- **REST API** entre les composants  
- **Protocoles propriétaires** pour la communication avec les capteurs  

---

## 🔹 Fonctionnalités Clés

### 📏 **Décompression**
- Calcul et modélisation **en temps réel** de la saturation/désaturation de l’azote  
- Intégration des **algorithmes Bühlmann** et des **tables MN90**  
- Gestion des **paliers de sécurité** et recommandations après plongée  

### 🧭 **Navigation**
- Détermination de la **profondeur** et de la **position GPS**  
- Guidage vers un **point de sortie** (ex : bateau)  
- Cartographie et **historique des plongées**  

### 📸 **Captation Vidéo/Photo**
- **Enregistrement des fonds marins** en Full HD  
- Stockage au format **.raw**  
- **Focus automatique**  

### 📅 **Planification des Plongées**
- **Simulation** des plongées à l’avance  
- Calcul des **temps de plongée** et des **paliers nécessaires**  
- Utilisation d’algorithmes comme **Pydplanner**  

### 📊 **Gestion et Analyse**
- Édition des **statistiques de plongée**  
- Visualisation des **zones de plongée**  
- **Paramétrage et configuration** du SDC  

---

## 📌 Livrables
📖 **Documentation**  
- Cahier des charges (**Template IEEE**)  
- Spécifications des exigences fonctionnelles  
- Spécifications des interfaces  

💻 **Logiciels**  
- **SDC** : Application du calculateur  
- **DB** : Gestion des historiques  
- **Mgt** : Application de gestion  

---

## 🚀 Installation et Exécution

### 📥 1. Prérequis
Assurez-vous d’avoir installé :  
- **Python 3.x**  
- **pip** (gestionnaire de paquets Python)  
- **Docker** (optionnel pour exécuter la base de données)  

### 🔧 2. Installation
Clonez ce dépôt Git et installez les dépendances :
```bash
git clone https://github.com/votre-utilisateur/smart-dive-computer.git
cd smart-dive-computer
pip install -r requirements.txt
