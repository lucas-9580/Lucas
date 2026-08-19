# 📚 Exercice : Introduction à Git/GitHub et Présentations

## Objectifs
À la fin de cet exercice, vous serez capable de :
- ✅ Comprendre la différence entre un dépôt local et distant
- ✅ Créer, forker et cloner un dépôt distant
- ✅ Effectuer des modifications et les pousser (push) vers le dépôt distant
- ✅ Collaborer en donnant accès au professeur
- ✅ Créer votre première présentation personnelle

---

## 📋  Concepts Fondamentaux

### 1.1 Dépôt Local vs Distant
- **Dépôt Local** : Copie complète de votre projet sur votre ordinateur (`.git/`)
- **Dépôt Distant** : Copie du projet hébergée sur un serveur (GitHub, GitLab, etc.)

### 1.2 Workflow Git de base
```
[Modifications locales] → git add → git commit → git push → [Dépôt distant]
```

---

## 🎯 Exercice Principal

### Phase 1 : Fork et Clone

**Objectif** : Créer votre propre copie du dépôt et le travailler localement

#### Tâches :
1. **Fork le dépôt** `vivgxojo/Presentations` sur GitHub
   - Aller sur https://github.com/vivgxojo/Presentations
   - Cliquer sur le bouton "Fork" en haut à droite
   - Sélectionner votre compte comme destination

2. **Clone votre fork localement**
   
---

### Phase 2 : Créer votre présentation

**Objectif** : Ajouter un fichier Python personnalisé avec votre présentation

#### Tâches :

1. **Consulter l'exemple existant**
   

2. **Créer votre propre fichier de présentation**
   presentations_VOTRE_NOM.py
   
3. **Ajouter votre présentation (exemple)**
   ```python
   """
   Présentation personnelle - [Votre Nom]
   """
   nom = "Votre Nom"
   prenom = "Votre Prénom"
   email = "votre.email@example.com"
   universite = "Université/École"
   specialite = "Votre Spécialité"
   interet_principal = "Vos intérêts (ex: IA, Web, DevOps)"
   experience_git = "Débutant/Intermédiaire/Avancé"
   #...
   ```

4. **Tester votre fichier**
   
---

### Phase 3 : Versionner et Pousser vos Modifications

**Objectif** : Enregistrer et envoyer vos modifications au dépôt distant

#### Tâches :

1. **Ajouter votre fichier au staging area si c'est pas déjà fait**

2. **Créer un commit avec un message descriptif**

3. **Pousser vers votre dépôt distant**

4. **Vérifier sur GitHub**
   - Aller sur votre fork : `https://github.com/VOTRE_USERNAME/Presentations`
   - Vérifier que vos fichiers sont présents

---

### Phase 4 : Collaborer avec le Professeur

**Objectif** : Donner accès au professeur et créer une Pull Request

#### Tâches :

**Option A : Collaborateur Direct (si demandé)**
1. Aller dans "Settings" → "Collaborators"
2. Ajouter l'utilisateur GitHub du professeur : vivgxojo
3. Le professeur peut maintenant accéder à votre présentation.


## ✅ Critères d'Acceptation

Votre exercice sera validé si :
- [ ] Votre fork est créé et cloné localement
- [ ] Un fichier `presentations_[votre_nom].py` est créé
- [ ] Le fichier contient au minimum :
  - Votre nom et prénom
  - Votre email
  - Vos intérêts/spécialités
  - Une fonction pour afficher les informations
- [ ] Les modifications sont commitées avec un message clair
- [ ] Les modifications sont pushées vers GitHub
- [ ] Le code Python est fonctionnel (pas d'erreurs à l'exécution)

---

## 📚 Ressources Complémentaires

- [Git Documentation Officielle](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Visualiser Git](https://git-school.github.io/visualizing-git/)
- [Branching Model](https://nvie.com/posts/a-successful-git-branching-model/)


**Bonne chance ! 🚀**
