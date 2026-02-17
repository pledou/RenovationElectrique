# Plan d'Organisation Interne du Tableau Électrique (Mode Opératoire)

## Date
17 février 2026

## Objectif du document
Ce document est le **mode opératoire chantier**.

Il ne porte pas la justification normative, le chiffrage détaillé ni les arbitrages d'architecture. Ces éléments sont maintenus dans le document maître :
- [proposition_tableau_electrique.md](proposition_tableau_electrique.md)

---

## Rôle de ce document vs document maître

- **Document maître** : [proposition_tableau_electrique.md](proposition_tableau_electrique.md)
  - Référentiel technique unique (NF C 15-100, calibres, sections, logique énergétique, coûts, délais)
- **Présent document** : exécution terrain
  - Implantation du coffret
  - Ordre de montage/raccordement
  - Repérage, tests, relevés, contrôle final

> En cas d'écart, **la proposition technique fait foi**.

---

## Configuration retenue (rappel synthétique)

- Tableau principal : **3 rangées × 13 modules**
- Modules utilisés : **24**
- Modules libres : **15**
- Sous-tableau étage : **supprimé**
- Circuits étage intégrés : **VMI, P5, L3, L4, P6, P7**

Référence détaillée (affectations exactes par module, calibres, sections) :
- [proposition_tableau_electrique.md](proposition_tableau_electrique.md)

---

## Affectation opérationnelle par rangée

### Rangée 1 (Type A)
- ID 40A 30mA Type A (modules 1-2)
- P1, P2, P3, P4, Onduleur, Microonduleurs, VMI
- Réserve : 4 modules

### Rangée 2 (Type AC)
- ID 40A 30mA Type AC (modules 1-2)
- Chaudière + routeur ECS, L1, L2, L3, L4, mesure onduleur (2 modules), P5, P6, P7
- Réserve : 1 module

### Rangée 3 (Type A)
- ID 40A 30mA Type A (modules 1-2)
- ECS (chauffe-eau)
- Réserve : 10 modules

---

## Implantation physique (garage)

- Bas du coffret : **110–120 cm**
- Centre organes de manœuvre : **130–140 cm**
- Haut du coffret : **150–160 cm**
- Fixation : 4 points, support adapté au mur, niveau/aplomb vérifiés

---

## Placement des pinces ampèremétriques

### Pince 1 (mesure globale)
- Position : arrivée principale **après disjoncteur EDF** et avant répartition des rangées
- Usage : pilotage flux global (import/injection)

### Pince 2 (mesure hors ECS)
- Position : alimentation des **rangées 1 + 2 uniquement**
- Usage : mesure consommation maison hors ECS pour la régulation batterie/onduleur

Référence logique énergétique complète :
- [proposition_tableau_electrique.md](proposition_tableau_electrique.md)

---

## Procédure de réalisation

### Étape 1 — Préparation (hors tension non requise)
1. Poser le nouveau coffret à côté de l'existant
2. Monter différentiels, peignes, borniers, obturateurs
3. Préparer les disjoncteurs (récupérés + neufs)
4. Préparer l'étiquetage des conducteurs

### Étape 2 — Bascule tableau principal (hors tension obligatoire)
1. Coupure générale + VAT
2. Bascule **circuit par circuit**
3. Vérification fonctionnelle après chaque bascule
4. Circuits prioritaires traités en dernier (chaudière, froid)

### Étape 3 — Intégration des circuits étage
1. Déposer le sous-tableau étage
2. Tirer les 6 liaisons directes vers le tableau principal
3. Ajuster le passage combles (parpaing) et protéger mécaniquement
4. Raccorder sur les départs dédiés

### Étape 4 — Validation
1. Test bouton TEST de chaque différentiel
2. Contrôle isolement / continuité terre
3. Vérification déclenchements et réarmements
4. Mise à jour repérage + schéma sur porte

---

## Checklist chantier (compacte)

### Avant intervention
- [ ] Matériel complet (coffret, ID, DJ, peignes, borniers, consommables)
- [ ] Outils et EPI disponibles
- [ ] Plan de repérage imprimé

### Pendant intervention
- [ ] Coupure générale + VAT validées
- [ ] Repérage de chaque conducteur avant déconnexion
- [ ] Serrage au couple constructeur
- [ ] Séparation stricte des neutres par différentiel

### Après intervention
- [ ] Tests différentiels OK
- [ ] Fonctionnement de tous les circuits OK
- [ ] Mesures d'isolement consignées
- [ ] Étiquetage final en place
- [ ] Schéma unifilaire posé sur porte

---

## Repérage et étiquetage

Méthode retenue : scotch de peintre + marquage lisible au crayon bic.

Références de repérage :
- [etiquettes_tableau.md](etiquettes_tableau.md)
- [schema_unifilaire_tableau.drawio](schema_unifilaire_tableau.drawio)

---

## Points de vigilance sécurité et conformité

- Coupure générale et VAT systématiques
- Respect des sections et calibres définis dans la proposition
- Neutres séparés par différentiel
- Contrôle des défauts existants non traités par ce lot (prises sans terre, hors conduit, croisements L1/L2/L3)

Référence complète des non-conformités à traiter ultérieurement :
- [proposition_tableau_electrique.md](proposition_tableau_electrique.md)

---

## Relevés à compléter sur site

- [ ] Couleurs réelles des conducteurs
- [ ] Mesures d'isolement par circuit
- [ ] Mesures de fuite avant/après
- [ ] Photos avant / pendant / après
- [ ] Position finale validée des pinces 1 et 2

---

## Documents liés

- [proposition_tableau_electrique.md](proposition_tableau_electrique.md) (référentiel technique)
- [plan_implantation_tableau.md](plan_implantation_tableau.md)
- [schema_unifilaire_tableau.drawio](schema_unifilaire_tableau.drawio)
- [metré_rallonges_cables.md](metré_rallonges_cables.md)
- [checklist_validation.md](checklist_validation.md)

---

**Auteur** : GitHub Copilot  
**Date** : 17 février 2026  
**Version** : 2.0  
**Statut** : ✅ Version opératoire alignée sur la proposition technique
