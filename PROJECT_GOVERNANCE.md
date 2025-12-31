# Project Governance

## 1. Objectif de ce document

Ce document définit les règles de gouvernance du projet.  
Il sert de **référence unique** pour :

- la prise de décision
- la gestion du périmètre
- les responsabilités
- le cycle de vie du projet
- la définition du travail terminé (“Definition of Done”)

Toute contribution au projet **doit respecter ce document**.

---

## 2. Principes fondamentaux

Le projet repose sur les principes suivants :

- **Clarté avant vitesse**
- **Automatisation avant intervention humaine**
- **Traçabilité totale**
- **Simplicité (KISS)**
- **Responsabilité individuelle**
- **Qualité non négociable**

Aucune règle implicite n’est acceptée :  
*si ce n’est pas écrit, ce n’est pas une règle.*

---

## 3. Source de vérité (Single Source of Truth)

| Élément | Outil |
|------|------|
| Code source | GitHub Repository |
| Tâches / bugs / évolutions | GitHub Issues |
| Avancement projet | GitHub Projects |
| Décisions techniques | Documentation (`/docs`) |
| Historique des changements | Git (commits + tags) |
| Releases | GitHub Releases |

Aucun suivi parallèle (Notion, Excel, Slack, email, etc.) n’est autorisé.

---

## 4. Rôles et responsabilités

### 4.1 Product Owner (PO)
Responsable de **ce qui doit être fait**.

- Définit la vision produit
- Priorise le backlog
- Valide fonctionnellement les livraisons
- Accepte ou refuse une issue terminée

### 4.2 Tech Lead
Responsable de **comment c’est fait**.

- Définit l’architecture
- Valide les choix techniques
- Garantit la qualité du code
- Statue sur la dette technique

### 4.3 Développeur
Responsable de **ce qu’il livre**.

- Implémente les issues
- Respecte les standards
- Écrit les tests
- Documente son travail
- Corrige les problèmes détectés en CI

### 4.4 Maintainer
Responsable de **la stabilité du projet**.

- Gère les releases
- Supervise la CI/CD
- Administre les accès
- Valide les merges critiques

> Une même personne peut cumuler plusieurs rôles.

---

## 5. Cycle de vie d’une fonctionnalité

1. Création d’une **Issue**
2. Qualification et priorisation
3. Assignation
4. Développement sur branche dédiée
5. Pull Request
6. Revue de code
7. Validation CI
8. Merge
9. Release automatique
10. Déploiement

Aucune étape ne peut être sautée.

---

## 6. Gestion du périmètre (Scope Control)

### Règles

- Toute évolution **doit passer par une Issue**
- Aucun ajout fonctionnel “rapide” n’est accepté
- Les changements de périmètre sont explicitement documentés

### Hors périmètre

- Refactorings non justifiés
- Optimisations prématurées
- Fonctionnalités non demandées (YAGNI)

---

## 7. Prise de décision

### Niveaux de décision

| Type | Décideur |
|----|----|
| Fonctionnel | Product Owner |
| Technique | Tech Lead |
| Architecture | Tech Lead / Maintainer |
| Sécurité | Maintainer |

### Règle clé

> Toute décision structurante doit être **documentée**  
> dans un fichier `ADR` (Architecture Decision Record).

---

## 8. Definition of Done (DoD)

Une issue est considérée comme **terminée** si et seulement si :

- [ ] Le code est implémenté
- [ ] Les tests sont écrits et passent
- [ ] La CI est verte
- [ ] La documentation est à jour
- [ ] Le code respecte les standards
- [ ] La PR est validée
- [ ] La fonctionnalité est déployable

Sinon, l’issue reste **ouverte**.

---

## 9. Qualité & tolérance à l’erreur

- **Tolérance zéro** pour :
  - le code cassé sur `main`
  - les secrets exposés
  - la CI ignorée

- **Les erreurs sont acceptées**
  - si elles sont détectées tôt
  - si elles sont corrigées proprement
  - si elles améliorent le système

---

## 10. Évolution de la gouvernance

Ce document peut évoluer.

Toute modification :
- doit être proposée via une Pull Request
- doit être discutée
- doit être acceptée par le Maintainer

---

## 11. Engagement des contributeurs

Contribuer à ce projet implique :

- accepter cette gouvernance
- respecter les standards
- contribuer à l’amélioration continue

> **La qualité du projet est une responsabilité collective.**
