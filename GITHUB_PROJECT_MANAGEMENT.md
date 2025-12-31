# Gestion de projet sur GitHub

## 1. Objectif de ce document

Ce document définit les standards de gestion de projet sur GitHub.

GitHub est utilisé comme **outil unique de pilotage**, de la demande initiale
jusqu’au déploiement en production.

Les objectifs sont :
- une traçabilité complète
- une visibilité claire de l’avancement
- une intégration rapide des nouveaux contributeurs
- une automatisation maximale

---

## 2. Principe fondamental

> **Tout ce qui n’est pas dans GitHub n’existe pas.**

Aucune tâche, bug, discussion structurante ou décision projet ne doit exister
en dehors de GitHub.

---

## 3. GitHub Issues : unité de travail unique

### 3.1 Règle absolue

**Une issue = une unité de travail claire et traçable**

Toute modification du projet (code, documentation, infra, process) doit être liée
à **une issue GitHub**.

---

### 3.2 Types d’issues standardisés

Chaque issue doit appartenir à **un type explicite** :

| Type | Description |
|---|---|
| `feature` | Nouvelle fonctionnalité |
| `bug` | Dysfonctionnement |
| `tech-debt` | Dette technique |
| `refactor` | Refactorisation sans impact fonctionnel |
| `docs` | Documentation |
| `chore` | Tâche technique non fonctionnelle |
| `security` | Problème de sécurité |

Le type est matérialisé par un **label obligatoire**.

---

### 3.3 Règles de création d’une issue

Une issue valide doit contenir :

- un **titre clair et actionnable**
- une **description explicite**
- un **objectif mesurable**
- des **critères d’acceptation**
- un **type (label)**

 Une issue vague ou ambiguë sera rejetée.

---

## 4. Templates d’issues

Tous les types d’issues utilisent des **templates Markdown obligatoires**.

### Templates requis

- `feature.md`
- `bug.md`
- `tech-debt.md`
- `refactor.md`
- `docs.md`
- `security.md`

Aucun contenu libre non structuré n’est accepté.

---

## 5. Labels standardisés

### 5.1 Labels de type (obligatoires)

- `type:feature`
- `type:bug`
- `type:tech-debt`
- `type:refactor`
- `type:docs`
- `type:chore`
- `type:security`

---

### 5.2 Labels de priorité

- `priority:low`
- `priority:medium`
- `priority:high`
- `priority:critical`

---

### 5.3 Labels de statut

- `status:triage`
- `status:ready`
- `status:in-progress`
- `status:blocked`
- `status:review`
- `status:done`

---

### 5.4 Labels transverses

- `breaking-change`
- `good-first-issue`
- `help-wanted`
- `needs-discussion`

---

## 6. GitHub Projects (pilotage)

### 6.1 Projet officiel

Chaque repository dispose d’**un GitHub Project officiel**.

Ce projet est :
- la vue backlog
- la vue avancement
- la vue roadmap

---

### 6.2 Colonnes standard

| Colonne | Description |
|---|---|
| Backlog | Issues non planifiées |
| Ready | Issues prêtes à être développées |
| In Progress | En cours |
| Review | En revue |
| Blocked | Bloquées |
| Done | Terminées |

Une issue doit toujours être **dans une seule colonne**.

---

### 6.3 Règles de déplacement

- Le déplacement manuel est autorisé
- Les automatisations sont privilégiées
- Une issue ne peut pas être en `In Progress` sans être assignée

---

## 7. Assignation & responsabilité

### Règles

- Une issue `In Progress` doit avoir **un responsable unique**
- Le responsable est garant :
  - du respect des standards
  - de la livraison
  - de la mise à jour de l’issue

Pas d’issue “orpheline”.

---

## 8. Lien Issue ↔ Code

### Obligations

- Chaque branche est liée à **une issue**
- Chaque PR référence **au moins une issue**
- Les commits doivent référencer l’issue (`#123`)

La traçabilité doit être **automatique et complète**.

---

## 9. Milestones & Roadmap

### 9.1 Milestones

Les milestones représentent :
- une version
- une échéance
- un lot fonctionnel

Chaque issue **peut** être rattachée à une milestone.

---

### 9.2 Règles

- Une milestone doit être fermée
- Une milestone fermée déclenche une release
- Les issues non terminées sont reportées explicitement

---

## 10. Automatisations GitHub

### Automatisations attendues

- Ajout automatique au Project
- Mise à jour du statut selon la PR
- Passage en `Done` au merge
- Fermeture automatique via commit / PR

Les automatisations réduisent l’erreur humaine.

---

## 11. Historique & auditabilité

GitHub doit permettre à tout moment de répondre à :

- Pourquoi cette décision ?
- Quand cela a été fait ?
- Par qui ?
- Dans quelle version ?

Si la réponse n’est pas traçable, le process est incomplet.

---

## 12. Règles de discipline

- Une issue = un sujet
- Une PR = une issue (ou un petit groupe cohérent)
- Aucun travail non tracé n’est accepté
- La qualité de suivi est aussi importante que le code

---

## 13. Amélioration continue

Les standards de gestion de projet peuvent évoluer.

Toute évolution :
- passe par une issue
- est discutée
- est documentée
- est validée par un Maintainer

---

> **Un projet bien suivi est un projet qui scale.**
