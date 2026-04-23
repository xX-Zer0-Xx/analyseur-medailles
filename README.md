# 📚 Analyseur de Bibliothèque

Projet Python - L1 Informatique, Semestre 1  
Auteur : [Ton Prénom Nom]  
Date : Avril 2025

---

## C'est quoi ce programme ?

C'est un programme Python qui lit un fichier de données sur des livres empruntés dans une bibliothèque, et permet de faire des recherches et des statistiques dessus.

On peut par exemple savoir quel livre a été le plus emprunté en 2023, voir le top 10 de tous les temps, ou encore trouver la meilleure année d'un auteur.

---

## Ce qu'il faut avoir installé

Juste **Python 3** sur ton ordinateur. Pas besoin d'installer quoi que ce soit en plus, on utilise uniquement des modules qui sont déjà inclus avec Python (`csv` et `random`).

Pour vérifier que Python est installé, ouvre un terminal et tape :

```
python --version
```

Si tu vois un numéro de version (genre `Python 3.11.2`), c'est bon.

---

## Les fichiers du projet

```
analyseur-bibliotheque/
│
├── analyseur.py      ← le programme principal, c'est lui qu'on lance
├── livres.csv        ← le fichier de données (ne pas modifier !)
└── README.md         ← ce fichier
```

> ⚠️ Important : `analyseur.py` et `livres.csv` doivent être dans le **même dossier**. Si tu mets le CSV ailleurs, le programme ne le trouvera pas.

---

## Comment lancer le programme

**Étape 1** — Ouvre un terminal (sous Windows : clic droit dans le dossier → "Ouvrir dans le terminal")

**Étape 2** — Va dans le dossier du projet :

```
cd chemin/vers/le/dossier
```

**Étape 3** — Lance le programme :

```
python analyseur.py
```

Et c'est tout ! Un menu apparaît et tu n'as plus qu'à taper un chiffre.

---

## Le fichier livres.csv — comment il est structuré

C'est un fichier texte avec des colonnes séparées par des `;`. La première ligne contient les noms des colonnes, les suivantes les données.

```
titre;auteur;annee_emprunt;nb_emprunts
Harry Potter et la Pierre Philosophale;J.K. Rowling;2020;45
Le Petit Prince;Antoine de Saint-Exupery;2021;30
...
```

| Colonne | Ce que ça contient |
|---|---|
| `titre` | Le titre du livre |
| `auteur` | Le nom de l'auteur |
| `annee_emprunt` | L'année concernée |
| `nb_emprunts` | Le nombre de fois emprunté cette année-là |

Un même livre peut apparaître plusieurs fois s'il a été emprunté sur plusieurs années.

---

## Ce que le programme peut faire

Une fois lancé, un menu apparaît avec 7 options :

**Option 1 — Livre le plus emprunté en 2023**  
Affiche le livre qui a eu le plus d'emprunts pendant l'année 2023.

**Option 2 — Première année d'emprunt d'un livre**  
Tu entres un titre, et le programme te dit depuis quelle année il est dans la bibliothèque.

**Option 3 — Année de succès d'un auteur**  
Tu entres un nom d'auteur, et le programme te dit quelle année a été la meilleure pour lui (avec le détail année par année).

**Option 4 — Top 10 des livres**  
Classement des 10 livres les plus empruntés, toutes années confondues.

**Option 5 — Livres d'une année précise**  
Tu entres une année, et le programme liste tous les livres empruntés cette année-là.

**Option 6 — Livre aléatoire**  
Le programme pioche un livre au hasard dans la base. Pratique si tu cherches une idée de lecture !

**Option 7 — Statistiques générales**  
Donne une vue d'ensemble : nombre total d'emprunts, moyenne, nombre d'auteurs différents, années couvertes.

**Option 0 — Quitter**  
Ferme le programme proprement.

---

## Exemple de ce qu'on voit à l'écran

```
Fichier chargé avec succès !
Nombre de lignes lues : 30

Bienvenue dans l'Analyseur de la Bibliothèque !

==================================================
   ANALYSEUR DE LA BIBLIOTHEQUE
==================================================
1. Livre le plus emprunté en 2023
2. Première année où un livre a été emprunté
3. Année de succès d'un auteur
4. Top 10 des livres toutes années confondues
5. Livres d'une année précise
6. Livre aléatoire (surprise !)
7. Statistiques générales
0. Quitter
==================================================
Votre choix : 1

--- Livre le plus emprunté en 2023 ---
Titre  : Le Petit Prince
Auteur : Antoine de Saint-Exupery
Nombre d'emprunts : 55
```

---

## Si ça ne marche pas

**Le programme dit "fichier introuvable"**  
→ Vérifie que `livres.csv` est bien dans le même dossier que `analyseur.py`.

**Le programme ne se lance pas du tout**  
→ Vérifie que Python est bien installé avec `python --version`. Sur certains ordinateurs, il faut écrire `python3` au lieu de `python`.

**Les accents s'affichent mal dans le terminal**  
→ C'est un problème d'encodage du terminal Windows. Tape cette commande avant de lancer le programme :
```
chcp 65001
```

---

## Ce qu'on a utilisé en Python

Tout ce qui est dans ce programme a été vu en cours :

- Les **variables** et les **types** (int, str...)
- Les **listes** et les **dictionnaires**
- Les **boucles** `for` et `while`
- Les **conditions** `if / elif / else`
- Les **fonctions** avec `def`
- La **lecture de fichier** avec `open()` et le module `csv`
- Le module `random` pour le livre surprise
- Un **tri à bulles** codé à la main pour le top 10

---

*Projet réalisé dans le cadre du cours d'Introduction à Python — L1 Informatique S1*
