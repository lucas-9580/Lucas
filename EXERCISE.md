# 📚 Exercice : Introduction à Git/GitHub

## Objectifs
À la fin de cet exercice, vous serez capable de :
- ✅ Comprendre la différence entre un dépôt local et distant
- ✅ Créer, forker et cloner un dépôt distant
- ✅ Effectuer des modifications et les pousser (push) vers le dépôt distant
- ✅ Collaborer en donnant accès au professeur
- ✅ Créer votre première présentation personnelle

---

## 📋 Partie 1 : Concepts Fondamentaux

### 1.1 Dépôt Local vs Distant
- **Dépôt Local** : Copie complète de votre projet sur votre ordinateur (`.git/`)
- **Dépôt Distant** : Copie du projet hébergée sur un serveur (GitHub, GitLab, etc.)

### 1.2 Workflow Git de base
```
[Modifications locales] → git add → git commit → git push → [Dépôt distant]
```

---

## 🛠️ Partie 2 : Préparation de l'Environnement

### Étape 1 : Installer Git
```bash
# macOS (avec Homebrew)
brew install git

# Ubuntu/Debian
sudo apt-get install git

# Windows
# Télécharger depuis https://git-scm.com/download/win
```

### Étape 2 : Configuration initiale de Git
```bash
git config --global user.name "Votre Nom"
git config --global user.email "votre.email@example.com"
```

### Étape 3 : Générer une clé SSH (optionnel mais recommandé)
```bash
ssh-keygen -t ed25519 -C "votre.email@example.com"
# Suivre les instructions et ajouter la clé publique à GitHub
cat ~/.ssh/id_ed25519.pub
```

---

## 🎯 Partie 3 : Exercice Principal

### Phase 1 : Fork et Clone

**Objectif** : Créer votre propre copie du dépôt et le travailler localement

#### Tâches :
1. **Fork le dépôt** `vivgxojo/Presentations` sur GitHub
   - Aller sur https://github.com/vivgxojo/Presentations
   - Cliquer sur le bouton "Fork" en haut à droite
   - Sélectionner votre compte comme destination

2. **Clone votre fork localement**
   ```bash
   git clone https://github.com/VOTRE_USERNAME/Presentations.git
   cd Presentations
   ```

3. **Ajouter le dépôt upstream (optionnel mais recommandé)**
   ```bash
   git remote add upstream https://github.com/vivgxojo/Presentations.git
   git remote -v  # Vérifier les remotes
   ```

---

### Phase 2 : Créer votre présentation

**Objectif** : Ajouter un fichier Python personnalisé avec votre présentation

#### Tâches :

1. **Consulter l'exemple existant**
   ```bash
   cat presentations.py
   ```

2. **Créer votre propre fichier de présentation**
   ```bash
   touch presentations_VOTRE_NOM.py
   # Ou créer un nouveau fichier presentations_[votre_nom].py
   ```

3. **Ajouter votre présentation (exemple)**
   ```python
   """
   Présentation personnelle - [Votre Nom]
   """

   class Presentation:
       def __init__(self):
           self.nom = "Votre Nom"
           self.prenom = "Votre Prénom"
           self.email = "votre.email@example.com"
           self.universite = "Université/École"
           self.specialite = "Votre Spécialité"
           self.interet_principal = "Vos intérêts (ex: IA, Web, DevOps)"
           self.experience_git = "Débutant/Intermédiaire/Avancé"

       def __str__(self):
           return f"""
   ╔══════════════════════════════════════╗
   ║        PRÉSENTATION PERSONNELLE       ║
   ╠══════════════════════════════════════╣
   ║ Nom        : {self.nom:^26}║
   ║ Prénom     : {self.prenom:^26}║
   ║ Email      : {self.email:^26}║
   ║ Université : {self.universite:^26}║
   ║ Spécialité : {self.specialite:^26}║
   ║ Intérêts   : {self.interet_principal:^26}║
   ║ Exp. Git   : {self.experience_git:^26}║
   ╚══════════════════════════════════════╝
           """

       def say_hello(self):
           return f"Bonjour! Je suis {self.prenom} {self.nom}"

   if __name__ == "__main__":
       me = Presentation()
       print(me)
       print(me.say_hello())
   ```

4. **Tester votre fichier**
   ```bash
   python presentations_VOTRE_NOM.py
   ```

---

### Phase 3 : Versionner et Pousser vos Modifications

**Objectif** : Enregistrer et envoyer vos modifications au dépôt distant

#### Tâches :

1. **Vérifier le statut des fichiers**
   ```bash
   git status
   ```

2. **Ajouter vos fichiers au staging area**
   ```bash
   git add presentations_VOTRE_NOM.py
   # Ou pour ajouter tous les fichiers modifiés:
   git add .
   ```

3. **Créer un commit avec un message descriptif**
   ```bash
   git commit -m "feat: add my personal presentation - [Your Name]"
   # Format recommandé:
   # feat: description
   # fix: description
   # docs: description
   # refactor: description
   ```

4. **Pousser vers votre dépôt distant**
   ```bash
   git push origin main
   # ou
   git push origin master
   ```

5. **Vérifier sur GitHub**
   - Aller sur votre fork : `https://github.com/VOTRE_USERNAME/Presentations`
   - Vérifier que vos fichiers sont présents

---

### Phase 4 : Collaborer avec le Professeur

**Objectif** : Donner accès au professeur et créer une Pull Request

#### Tâches :

**Option A : Collaborateur Direct (si demandé)**
1. Aller dans "Settings" → "Collaborators"
2. Ajouter l'utilisateur GitHub du professeur
3. Le professeur peut maintenant commit directement

**Option B : Pull Request (recommandé)**
1. Depuis votre fork, cliquer sur "Pull Requests"
2. Cliquer sur "New Pull Request"
3. S'assurer que :
   - Base repository : `vivgxojo/Presentations` (main)
   - Head repository : `VOTRE_USERNAME/Presentations` (main)
4. Ajouter un titre et une description :
   ```
   Titre: Add [Your Name] presentation

   Description:
   - Personal presentation file added
   - Following the Git/GitHub exercise guidelines
   - Ready for review
   ```
5. Cliquer sur "Create Pull Request"
6. Le professeur recevra une notification et pourra l'examiner

---

## 📝 Commandes Git Essentielles

| Commande | Description |
|----------|-------------|
| `git init` | Initialiser un dépôt local |
| `git clone <URL>` | Cloner un dépôt distant |
| `git status` | Vérifier l'état du dépôt |
| `git add <fichier>` | Ajouter un fichier au staging |
| `git commit -m "msg"` | Enregistrer les modifications |
| `git push` | Pousser vers le dépôt distant |
| `git pull` | Récupérer les modifications du distant |
| `git branch` | Lister/créer les branches |
| `git checkout -b <branche>` | Créer et basculer vers une branche |
| `git log` | Voir l'historique des commits |

---

## 🔍 Dépannage Courant

### ❌ "fatal: not a git repository"
```bash
# Vous n'êtes pas dans le bon dossier
cd chemin/vers/Presentations
```

### ❌ "permission denied (publickey)"
```bash
# Problème SSH - vérifier votre clé SSH
ssh -T git@github.com
```

### ❌ "Updates were rejected because the tip of your current branch is behind"
```bash
# Faire un pull avant de push
git pull origin main
```

### ❌ "Changes not staged for commit"
```bash
# Vous avez modifié des fichiers mais pas les staged
git add .
git commit -m "votre message"
```

---

## ✅ Critères d'Acceptation

Votre exercice sera validé si :
- [ ] Votre fork est créé et cloné localement
- [ ] Un fichier `presentations_[votre_nom].py` est créé
- [ ] Le fichier contient au minimum :
  - Votre nom et prénom
  - Votre email
  - Vos intérêts/spécialités
  - Une méthode pour afficher les informations
- [ ] Les modifications sont commitées avec un message clair
- [ ] Les modifications sont pushées vers GitHub
- [ ] Une Pull Request est créée vers le dépôt principal
- [ ] Le code Python est fonctionnel (pas d'erreurs à l'exécution)

---

## 📚 Ressources Complémentaires

- [Git Documentation Officielle](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Visualiser Git](https://git-school.github.io/visualizing-git/)
- [Branching Model](https://nvie.com/posts/a-successful-git-branching-model/)

---

## 🤝 Support

En cas de problème :
1. Vérifier l'historique des commits : `git log`
2. Consulter le statut : `git status`
3. Demander de l'aide sur le forum ou à votre professeur
4. Envoyer votre Pull Request en indiquant vos questions

---

**Bonne chance ! 🚀**
