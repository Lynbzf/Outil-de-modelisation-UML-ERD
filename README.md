<h1 align="center">🖥️ Générateur UML/ERD</h1>
<p align="center">
<em>Outil interactif en Java & JavaFX pour créer et exporter des diagrammes UML et ERD, avec gestion avancée des entités, attributs et relations.</em>
</p>

<div align="center">

![Java](https://img.shields.io/badge/Java-17+-red.svg)
![JavaFX](https://img.shields.io/badge/JavaFX-UI_Library-blue.svg)
![IDE](https://img.shields.io/badge/IDE-Eclipse_IntelliJ-purple.svg)

</div>

Ce projet est un outil de génération et de modélisation de diagrammes **UML** (diagramme de classes) et **ERD** (entité-relation), développé en Java avec **JavaFX**. Il permet de créer des entités, attributs, relations et d’exporter des diagrammes de manière interactive.

---

## 1️ Guide de démarrage rapide

### 1.1 Lancement de l’application

- Sur **Linux** :  
  1. Naviguer vers le répertoire contenant `menu.sh`.  
  2. Rendre le script exécutable si nécessaire :  
     ```bash
     chmod +x menu.sh
     ```  
  3. Exécuter le script :  
     ```bash
     ./menu.sh
     ```  
  4. Le menu vérifie la présence de Java et lance l’interface graphique.

- Sur **Windows** :  
  1. Ouvrir l’invite de commande et naviguer vers le répertoire contenant `menu.bat`.  
  2. Exécuter :  
     ```cmd
     menu.bat
     ```  
  3. Si des erreurs apparaissent, exécuter `setup config.ps1` puis relancer `menu.bat`.  
  4. Vérifier que les variables d’environnement (ex : `JAVA_HOME`) sont correctement configurées.

L’interface principale contient :  
- **Barre d’outils gauche** : Création d’éléments de modélisation  
- **Zone centrale** : Zone de modélisation  
- **Panneau de propriétés droite** : Édition des détails des entités et attributs  

---

### 1.2 Choix du mode de modélisation

Utilisez les **boutons bascule** en haut de l’interface :  

- **UML** : Mode diagramme de classes (rectangles avec attributs listés)  
- **ERD** : Mode entité-relation (rectangles centraux avec attributs en cercles)  

---

## 2️ Création d’un modèle étape par étape

### 2.1 Étape 1 : Créer une entité

1. Dans la barre d’outils gauche, cliquez sur **Entité**  
2. Sélectionnez **+ Ajouter Entité**  
3. Un champ de saisie apparaît avec le texte `Entité`  
4. Double-cliquez pour éditer et saisir le nom (ex : `Client`, `Commande`)  
5. Appuyez sur **Entrée** pour valider  

> Résultat : L’entité apparaît dans la zone de modélisation et est automatiquement sauvegardée.

---

### 2.2 Étape 2 : Ajouter des attributs

#### Méthode 1 : Via la barre d’outils
1. Sélectionnez l’entité  
2. Cliquez sur **Attribut** puis **+ Ajouter Attribut**  
3. Double-cliquez sur le champ et saisissez le nom  
4. Appuyez sur **Entrée**

#### Méthode 2 : Via le panneau de propriétés
1. Sélectionnez l’entité  
2. Remplissez :  
   - **Nom de l’attribut**  
   - **Type** : `texte`, `int`, `float`, `bool`, `date`  
   - **PK** : cochez pour clé primaire  
   - **FK** : cochez pour clé étrangère  
3. Cliquez sur **Ajouter attribut**

---

### 2.3 Étape 3 : Gérer les clés

#### Clés primaires
1. Sélectionnez l’entité  
2. Cliquez sur **Clé primaire**  
3. Saisissez le nom de l’attribut  

#### Clés étrangères
1. Sélectionnez l’entité  
2. Cliquez sur **Clé étrangère**  
3. Saisissez le nom de l’attribut  

---

### 2.4 Étape 4 : Organiser le diagramme

- **Déplacer les entités** : clic + glisser  
- **Zoom & annulation** :  
  - `Ctrl + Molette` : zoom avant/arrière  
  - `Ctrl + Z` : annuler  
  - `Ctrl + Y` : rétablir  

---

## 3️3 Fonctionnalités avancées

### 3.1 Gestion des relations (ERD)
- Sélectionnez **Relation**  
- Connectez deux entités  

### 3.2 Système d’héritage (UML)
- Utilisez **Héritage** pour créer des relations parent-enfant  

### 3.3 Panneau de propriétés avancé
- Modifier nom d’entité, visualiser, ajouter ou supprimer des attributs  
- Types et clés PK/FK visibles  

---

## 4️ Menus et options

### 4.1 Menu Fichier
- Nouveau : créer un projet  
- Ouvrir : charger un projet  
- Enregistrer : sauvegarder  
- Quitter : fermer l’application  

### 4.2 Menu Édition
- Coller, Annuler, Rétablir  

### 4.3 Menu Vue
- Zoom avant (+) / Zoom arrière (-) / Réinitialiser la vue  

### 4.4 Menu Générer
- UML : exporter diagramme UML  
- ERD : exporter diagramme E&R  

---

## 5️ Différences UML vs ERD

| Mode | Description |
|------|------------|
| **UML** | Rectangles avec séparateurs, attributs listés verticalement, PK en rouge et gras, FK en orange, support de l’héritage |
| **ERD** | Entité centrale en rectangle, attributs en cercles, PK avec bordure dorée, FK en corail, relations visibles |

---

## 6️ Résolution de problèmes

### Problèmes courants
- **L’entité ne se crée pas** : vérifier doublons et appuyer sur Entrée  
- **Les attributs ne s’ajoutent pas** : sélectionner l’entité et vérifier les doublons  

---

## 7️ Structure des dossiers du projet

| Dossier | Description |
|--------|------------|
| **Encryption** | Gestion de la sécurité, configurations chiffrées, clés de chiffrement |
| **Java Code** | Classes Java de l’interface graphique et de la logique métier |
| **Backup** | Sauvegardes des fichiers du projet |
| **End user UMLGen** | Fichiers destinés aux utilisateurs finaux (exécutables, scripts) |
| **Ext driver** | Pilotes externes, bibliothèques tierces (PostgreSQL, etc.) |
| **JavaFX Lib** | Bibliothèques JavaFX nécessaires à l’interface graphique |
| **Manifest** | Fichiers de manifeste pour JAR, métadonnées et dépendances |
| **Proguard70** | Obfuscation et optimisation du code Java |
| **Script EU** | Scripts batch ou shell pour installation/mise à jour/exécution |

---

## 8️ Objectif pédagogique

Ce projet permet de démontrer :  
- Maîtrise de la programmation Java et JavaFX  
- Conception d’interfaces graphiques interactives  
- Gestion de la logique métier orientée objet  
- Création et manipulation de diagrammes UML et ERD  
- Exportation et sauvegarde de projets structurés
