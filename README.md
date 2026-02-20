Installer dans le répertoire de ce projet:  https://github.com/github/spec-kit/releases
GPT-5 mini possible

Passer Copilot en mode agent

Nouveau projet : https://youtu.be/THpWtwZ866s?t=293  / https://www.youtube.com/playlist?list=PL4cUxeGkcC9h9RbDpG8ZModUzwy45tLjb

Evol :  https://youtu.be/SGHIQTsPzuY


Voici un **guide détaillé** à destination d’élèves ingénieurs pour utiliser le framework Spec-KitCopilot dans le cadre d’un projet logiciel.

---

# Guide d’utilisation de Spec-KitCopilot pour élèves ingénieurs

## Objectif du framework

Spec-KitCopilot est un outil qui structure le développement logiciel en automatisant la rédaction des spécifications, la planification technique, la génération des tâches et la validation de la qualité.  
Il permet de travailler de façon professionnelle, collaborative et incrémentale.

speckit est une suite de commandes personnalisées pour ce projet, conçue pour vous guider dans la création d'une nouvelle fonctionnalité, de la description initiale au plan d'implémentation.

Voici les commandes disponibles et leur rôle apparent :

/speckit.specify: (Point de départ) Transforme une description en langage naturel en une spécification fonctionnelle détaillée.
/speckit.clarify: Pose des questions pour clarifier les exigences de la spécification.
/speckit.plan: Crée un plan de développement technique à partir de la spécification.
/speckit.analyze: Analyse la spécification ou le plan.
/speckit.implement: Probablement pour commencer l'implémentation du code.
/speckit.tasks: Crée ou gère des tâches de développement.
/speckit.checklist: Génère des listes de contrôle pour valider les étapes.
/speckit.taskstoissues: Convertit les tâches en "issues" (par exemple, sur GitHub).
/speckit.constitution: Affiche les règles et principes du projet.
Comment commencer :

Décrivez la fonctionnalité que vous souhaitez créer en utilisant la commande /speckit.specify.
Le système créera alors une nouvelle branche git, un fichier de spécification (spec.md) et une liste de contrôle de qualité.
Ensuite, vous pourrez utiliser /speckit.plan sur cette spécification pour générer le plan technique.

---

## 1. Prérequis

- Savoir utiliser Git et Visual Studio Code
- Avoir accès au dépôt du projet et aux scripts fournis
- Comprendre les principes de base de la gestion de projet logiciel (spécification, planification, tâches, tests)

---

## 2. Démarrage du projet

### a. Initialisation

1. **Cloner le dépôt** sur votre machine.
2. **Ouvrir le dossier** dans VS Code.

---

### b. Définir la première fonctionnalité

1. Dans le terminal, lancez la commande :
   ```
   /speckit.specify
   ```
2. **Décrivez la fonctionnalité** en une ou deux phrases claires (ex : "Permettre aux utilisateurs de s’inscrire et de se connecter").

---

## 3. Spécification et clarification

### a. Génération automatique

- Le framework crée une branche dédiée, un dossier de fonctionnalité et un fichier `spec.md` contenant les histoires utilisateur extraites de votre description.

### b. Clarification des exigences

1. Lancez :
   ```
   /speckit.clarify
   ```
2. **Répondez aux questions** posées par l’agent pour préciser les points flous (ex : "Quel type d’authentification ?").

---

## 4. Planification technique

1. Lancez :
   ```
   /speckit.plan
   ```
2. Le framework génère :
   - Un plan technique (`plan.md`)
   - Les modèles de données (`data-model.md`)
   - Les contrats d’API (`contracts/`)
   - La structure de fichiers recommandée

---

## 5. Génération des tâches

1. Lancez :
   ```
   /speckit.tasks
   ```
2. Le framework crée :
   - Un fichier `tasks.md` avec toutes les tâches à réaliser, organisées par histoire utilisateur et par phase

---

## 6. Validation de la qualité

1. Lancez :
   ```
   /speckit.checklist
   ```
2. Vérifiez que toutes les exigences sont claires, complètes et testables avant de commencer le développement.

---

## 7. Analyse de cohérence

1. Lancez :
   ```
   /speckit.analyze
   ```
2. L’agent vérifie la cohérence entre la spécification, le plan et les tâches, et signale les incohérences ou oublis.

---

## 8. Implémentation

- Suivez les tâches dans `tasks.md` :  
  Cochez chaque tâche terminée, respectez l’ordre et les dépendances.
- Travaillez en équipe : chaque membre peut prendre en charge une histoire utilisateur ou une phase.

---

## 9. Suivi et collaboration

1. Lancez :
   ```
   /speckit.taskstoissues
   ```
2. Les tâches sont converties en issues GitHub pour faciliter le suivi et la répartition du travail.

---

## 10. Conseils pour réussir

- **Rédigez des descriptions claires et précises** lors de la spécification.
- **Répondez sérieusement aux questions de clarification** : elles garantissent la qualité du projet.
- **Respectez la structure des fichiers générés** : cela facilite la relecture et la maintenance.
- **Utilisez les checklists** pour valider chaque étape avant de passer à la suivante.
- **Travaillez en incréments** : chaque histoire utilisateur doit être testable et livrable indépendamment.
- **Documentez vos décisions** dans les fichiers spec ou plan.
- **Collaborez via GitHub** : assignez les issues, suivez la progression, faites des revues de code.

---

## Exemple de workflow pour une équipe

1. **Spécification** : "Gestion des réservations"
2. **Clarification** : Type de réservation, gestion des conflits, notifications
3. **Planification** : Stack technique, modèles de données, API
4. **Tâches** : Création du modèle Reservation, endpoints API, tests unitaires
5. **Checklist** : Validation des exigences
6. **Analyse** : Vérification de la cohérence
7. **Implémentation** : Réalisation des tâches par les membres de l’équipe
8. **Suivi** : Issues GitHub pour chaque tâche

---

**Ce guide vous permet de structurer, planifier et réaliser un projet logiciel complexe en équipe, tout en garantissant la qualité et la traçabilité à chaque étape.**






---

Voici un exemple complet d’utilisation de `/speckit.specify` pour démarrer une nouvelle fonctionnalité avec Spec-KitCopilot :

## Exemple : Ajout d’une fonctionnalité "Gestion des commentaires"

### 1. Lancement de la commande

Dans le terminal, tapez :

```
/speckit.specify
```

### 2. Description de la fonctionnalité

Quand l’agent vous demande la description, saisissez :

> Permettre aux utilisateurs de publier, modifier et supprimer des commentaires sur chaque article du blog. Les commentaires doivent être modérés et chaque utilisateur ne peut modifier que ses propres commentaires.

---

### 3. Ce que le framework va générer

- **Branche dédiée** : `1-gestion-commentaires`
- **Dossier de fonctionnalité** : `specs/1-gestion-commentaires/`
- **Fichier de spécification** : `spec.md` contenant :
  - Histoires utilisateur (ex : "En tant qu’utilisateur, je peux publier un commentaire", "En tant qu’utilisateur, je peux modifier mon commentaire", "En tant que modérateur, je peux supprimer un commentaire inapproprié")
  - Priorités (P1, P2, P3…)
  - Scénarios d’acceptation pour chaque histoire
  - Exigences fonctionnelles et cas limites

---

### 4. Étapes suivantes

- Lancez `/speckit.clarify` pour répondre aux questions sur la modération, la gestion des droits, etc.
- Lancez `/speckit.plan` pour générer le plan technique (stack, modèles de données, endpoints API).
- Lancez `/speckit.tasks` pour obtenir la liste des tâches à réaliser (création du modèle Commentaire, endpoints, tests…).
- Utilisez `/speckit.checklist` et `/speckit.analyze` pour valider la qualité et la cohérence.

---

**Ce workflow vous permet de structurer et de piloter la réalisation de la fonctionnalité "Gestion des commentaires" de façon professionnelle et collaborative.**