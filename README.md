# Compte Rendu TP2 - GIT

**Nom :** Youssif Bassam Youssif  
**Département :** Informatique  
**Groupe :** TP-GIT équipe 10  
**Année :** 2024–2025  
**IUT :** Le Havre

---

## Objectifs du TP 2

Le but de ce deuxième TP est de commencer à travailler en autonomie avec un dépôt git distant.

---

## I. Création d’un compte sur GitHub

### 1. Compte GitHub créé 

---

## II. Ajout de la clé SSH au compte GitHub

### 1.1 Génération de la clé SSH
```bash
ssh-keygen -t rsa -b 4096 -C "youssifputrus@gmail.com"
```

### 1.2 Récupération de la clé
```bash
cat cat ~/.ssh/id_rsa.pub
```

### 1.3 Ajout de la clé sur GitHub
- Aller dans **Settings > SSH and GPG keys** sur GitHub
- Ajouter une nouvelle clé SSH
- Copier-coller le contenu de `id_rsa.pub`

 Clé SSH ajoutée avec succès

---

## III. Pousser un dépôt local existant (tp1) sur GitHub

### 1.1 Création du nouveau dépôt `tp1` sur GitHub (vide)

### 1.2 Ajout du lien du dépôt distant
```bash
origin  git@github.com:you8bssm/tp1.git (fetch)
origin  git@github.com:you8bssm/tp1.git (push)
```

### 1.3 Vérification
```bash
git remote -v
```

### 1.4 Connexion au dépôt distant
Connexion automatique via clé SSH si bien ajoutée 

### 1.5 Configuration de la branche principale
```bash
git branch -M main
```

### 1.6 Lien permanent avec le dépôt distant
```bash
git push -u origin main
```

### 1.7 Mise à jour du dépôt distant
```bash
git push
```

 Dépôt `tp1` synchronisé avec GitHub

---

## IV. Travail avec un dépôt distant

### 1.1 Pull (téléchargement de la dernière version du dépôt distant)
```bash
git pull
```

### 1.2 Historique des modifications
```bash
git log
```

### 1.3 Vérification du statut
```bash
git status
```

### 1.4 Ajout de fichiers
```bash
git add .
```

### 1.5 Commit des changements
```bash
git commit -m "Message clair du commit"
```

### 1.6 Push des modifications
```bash
git push
```

---

## V. Cloner un dépôt distant sur notre machine locale

### 1.1 Création d’un nouveau dossier `tp2`
```bash
mkdir tp2
cd tp2
```

### 1.2 Récupération de l’URL de clonage (SSH depuis GitHub)

### 1.3 Clonage du dépôt
```bash
git clone git@github.com:TonNomUtilisateur/tp2.git
```

### 1.4 Vérification
```bash
cd tp2
git status
```

### 1.5 Ajout, commit, et push dans le dépôt cloné
```bash
touch test.txt
echo "Hello GitHub" > test.txt
git add test.txt
git commit -m "Ajout d’un fichier de test"
git push
```

 Le dépôt distant a bien été cloné et modifié localement.

---
