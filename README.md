# NEXUS-FOOD
- Chaque recette a un **auteur**, une **version**, des **tags**, une **difficulté**, un **temps de prep** - Les autres cuisiniers peuvent **étoiler** (star), **forker**, **commenter**, **signaler des issues**, **proposer des PR** - Le classement "Tendances" calcule un **score de popularité** basé sur les étoiles et les forks

```markdown
# 🍔 NEXUS-FOOD

> **GitCook.com** — Le GitHub des cuisiniers.
> Versionne tes recettes. Fork les meilleures. Merge les idées.

<p align="center">
<img src="https://img.shields.io/badge/version-1.0.0-c8a45c?style=for-the-badge&labelColor=0d1117" />
<img src="https://img.shields.io/badge/python-3.8%2B-00d4ff?style=for-the-badge&labelColor=0d1117" />
<img src="https://img.shields.io/badge/sqlite-WAL-4ade80?style=for-the-badge&labelColor=0d1117" />
<img src="https://img.shields.io/badge/dependencies-ZERO-9d4edd?style=for-the-badge&labelColor=0d1117" />
<img src="https://img.shields.io/badge/license-NEXUS--OPEN--3.0-ff6ec7?style=for-the-badge&labelColor=0d1117" />
</p>

<p align="center">
<b>Un seul fichier Python. Zéro dépendance. Un réseau social culinaire complet.</b><br>
<i>Forgé par Aissa Mahammedi (DGK) — Code Nametron 3 Lara — Québec 2026</i>
</p>

---

## 🌟 C'est quoi NEXUS-FOOD ?

**NEXUS-FOOD** est un réseau social culinaire inspiré de GitHub, où chaque recette est un **dépôt versionné**, où chaque cuisinier est un **auteur**, et où les modifications sont des **pull requests**.

**Concept :**
- Chaque recette a un **auteur**, une **version**, des **tags**, une **difficulté**, un **temps de prep**
- Les autres cuisiniers peuvent **étoiler** (star), **forker**, **commenter**, **signaler des issues**, **proposer des PR**
- Le classement "Tendances" calcule un **score de popularité** basé sur les étoiles et les forks

**Pourquoi ?**
Parce que les recettes se transmettent de génération en génération, mais personne ne les **versionne**. Personne ne trace qui a modifié quoi, quand, et pourquoi. NEXUS-FOOD apporte la rigueur de Git à la cuisine.

---

## 🎯 Fonctionnalités

| Fonctionnalité | Description |
|----------------|-------------|
| **Recettes** | Création, édition, versions, fourks |
| **Utilisateurs** | Inscription, login, profil, bio |
| **Stars** | Compteur d'étoiles par recette |
| **Forks** | Dupliquer une recette + modifier |
| **Issues** | Signaler un bug, une allergie, une suggestion |
| **Pull Requests** | Proposer une modif structurée |
| **Commentaires** | Discussion sur chaque recette |
| **Tendances** | Classement par score (stars + forks × 2) |
| **Explorer** | Découverte aléatoire |
| **Auth** | Sessions via cookies HTTP-only |

---

## 🚀 Démarrage rapide

### Installation

**Prérequis :** Python 3.8+

**Aucune dépendance externe.**

```bash
# Clone
git clone https://github.com/Aissamohammedi88/nexus-food.git
cd nexus-food

# Lance
python3 forge_food.py
```

Accès

```
http://localhost:9984
```

Comptes de démonstration

Utilisateur Mot de passe Rôle
DGK nexus2026 Forgeron Suprême
Redman piment2026 Spécialiste piment
ChefMarie cuisine2026 Cuisine française
TacosKing tacos2026 Tacos cosmiques

---

📖 Utilisation

Créer une recette

1. Connecte-toi
2. Clique sur ➕ Créer
3. Remplis :
· Nom, description, difficulté (1-5), temps de prep, portions
· Ingrédients : nom | quantité (un par ligne)
· Étapes : une par ligne
· Tags : séparés par virgule
4. Valide

Exemple d'ingrédients :

```
Poulet | 150g
Pain brioché | 1
Cheddar | 2 tranches
Sauce DGK | 3 c.à.s
```

Forker une recette

1. Ouvre une recette
2. Clique sur Fork
3. Modifie ce que tu veux
4. Donne un nouveau nom
5. Valide → ta version est créée, la recette originale gagne +1 fork

Signaler une issue

1. Ouvre une recette
2. Section Signaler un problème
3. Choisis le label : bug, allergie, suggestion
4. Décris
5. Valide

Proposer un PR

1. Ouvre une recette
2. Section Proposer une modif
3. Titre + description + changements (format diff libre)
4. Valide → apparaît dans 🔀 PR

---

🏗️ Architecture

```
nexus-food/
├── forge_food.py # ~1500 lignes, tout en un
├── gitcock.db # SQLite (créé au démarrage)
└── README.md
```

Base de données

Table Contenu
users Cuisiniers
recipes Recettes versionnées
comments Commentaires
issues Signalements
pull_requests Propositions de modif
sessions Sessions HTTP

Mode SQLite : WAL (Write-Ahead Logging) pour concurrence.

---

🎨 Design

Thème : GitHub Dark + Touche Nexus

Couleur Hex Usage
Or #c8a45c Accent principal
Cyan #00d4ff Secondaire
Rose #ff6ec7 Accent vif
Violet #9d4edd Commentaires
Fond #0d1117 GitHub Dark
Carte #1c2128 Conteneurs
Bordure #30363d Séparateurs

Layout : Responsive mobile-first, sticky header, grille 2 colonnes.

---

🧠 Philosophie

La cuisine est un art de transmission. Mais la transmission perd de l'information :

· Grand-mère dit "un peu de sel" → personne ne sait combien
· Un ami ajoute "du thym" → personne ne trace qui a modifié
· Une recette se perd → personne ne sait où

NEXUS-FOOD résout ça. Chaque recette a :

· Une version (1.0, 2.0, 3.0…)
· Un auteur traçable
· Des forks qui gardent la lignée
· Des issues qui signalent les problèmes
· Des PR qui proposent des améliorations

C'est Git pour la cuisine. C'est GitCook.

---

🛠️ Technologies

Composant Technologie
Langage Python 3.8+
Serveur HTTP http.server (stdlib)
Base de données SQLite (stdlib)
Auth hashlib + secrets (stdlib)
Frontend HTML + CSS + formulaire POST
Dépendances externes AUCUNE

Zéro pip install. Zéro npm install. Zéro cargo. Juste Python.

---

📊 Statistiques

Métrique Valeur
Lignes de code ~1500
Fonctions ~25
Tables SQL 6
Pages 9
Dépendances 0
Temps de démarrage < 1s
Empreinte mémoire ~30 MB

---

🗺️ Roadmap

v1.1 — Q1 2027

□ Upload d'images de plats
□ Notation par étoiles (1-5) en plus du compteur
□ Recherche par ingrédient
□ Export d'une recette en PDF

v1.2 — Q2 2027

□ Fusion de PR (merge)
□ Fermeture d'issues
□ Notifications entre utilisateurs
□ Menu hebdomadaire

v2.0 — Q3 2027

□ Réécriture en Rust pour 10× plus rapide
□ Support fédéré (ActivityPub)
□ Application mobile

---

🤝 Contribuer

1. Fork le repo
2. Crée une branche (git checkout -b feat/ma-feature)
3. Commit (git commit -m 'feat: ajout feature')
4. Push (git push origin feat/ma-feature)
5. Ouvre une Pull Request

Règles

· Zéro dépendance externe (Python stdlib uniquement)
· Un fichier = tout le projet (contrainte volontaire)
· Docstring sur chaque fonction
· Testé manuellement avant PR

---

📜 Licence

NEXUS-OPEN-3.0

Copyright © 2026 Aissa Mahammedi (DGK)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.

---

🙏 Crédits

Auteur : Aissa Mahammedi (DGK)
Protocole : Code Nametron 3 Lara
Inspiration : GitHub, GitLab, Forks, PR
Localisation : Québec, Canada
Année : 2026

---

📞 Contact

· GitHub : @Aissamohammedi88
· LinkedIn : Aissa Mahammedi
· Issues : Ouvrir une issue sur ce repo

---

<p align="center">
<b>🍔 NEXUS-FOOD</b><br>
<i>Versionne tes recettes. Fork les meilleures. Merge les idées.</i><br>
<br>
<a href="https://github.com/Aissamohammedi88">
<img src="https://img.shields.io/badge/Forgé%20par-Aissa%20Mahammedi-c8a45c?style=for-the-badge&labelColor=0d1117" />
</a>
</p>
```---
