# Métré des Rallonges de Câbles

## Date
17 février 2026

## Hypothèses retenues

- Tableau principal unique en garage (110-150 cm).
- Sous-tableau étage supprimé.
- Liaison directe des circuits étage vers tableau principal : **10 m par circuit** (mesure terrain validée).
- Passage en combles possible avec **agrandissement local d'un trou dans le parpaing** si nécessaire.
- Câbles multiconducteurs RO2V : 3G1,5 / 3G2,5 / 3G6 / 3G10 mm².

---

## Circuits RdC à rallonger (référence existante)

Base conservée : **3,0 m par circuit**.

| Circuit       | Fonction           | Section | Longueur câble |
| ------------- | ------------------ | ------- | -------------- |
| Chaudière     | Chauffage          | 3G2,5   | 3,0 m          |
| L1            | Éclairage 1        | 3G1,5   | 3,0 m          |
| L2            | Éclairage 2        | 3G1,5   | 3,0 m          |
| P1            | Plaque cuisson     | 3G6     | 3,0 m          |
| P2            | Buanderie/Garage   | 3G2,5   | 3,0 m          |
| P3            | Séjour/Bureau/Four | 3G2,5   | 3,0 m          |
| P4            | Cuisine            | 3G2,5   | 3,0 m          |
| Sanitaire     | Chauffe-eau        | 3G2,5   | 3,0 m          |

---

## Circuits Étage en liaison directe (nouveau scénario)

Base validée : **10,0 m par circuit**.

| Circuit | Fonction              | Section | Longueur câble |
| ------- | --------------------- | ------- | -------------- |
| VMI     | Ventilation           | 3G1,5   | 10,0 m         |
| L3      | Éclairage étage       | 3G1,5   | 10,0 m         |
| L4      | Éclairage salle d'eau | 3G1,5   | 10,0 m         |
| P5      | Prises étage          | 3G2,5   | 10,0 m         |
| P6      | Prises chambre 3      | 3G2,5   | 10,0 m         |
| P7      | Prise palier          | 3G2,5   | 10,0 m         |

---

## Alimentation principale

| Câble                 | Section | Longueur |
| --------------------- | ------- | -------- |
| Arrivée EDF → Tableau | 3G10    | 3,0 m    |

---

## Synthèse des longueurs nécessaires

| Section | RdC  | Étage (direct 10m) | Total nécessaire |
| ------- | ---- | ------------------ | ---------------- |
| 3G1,5   | 6 m  | 30 m               | **36 m**         |
| 3G2,5   | 15 m | 30 m               | **45 m**         |
| 3G6     | 3 m  | 0 m                | **3 m**          |
| 3G10    | 3 m  | 0 m                | **3 m**          |

---

## Quantités à commander (avec marge chantier)

| Section | Total nécessaire | Quantité conseillée | Prix unitaire | Sous-total |
| ------- | ---------------- | ------------------- | ------------- | ---------- |
| 3G1,5   | 36 m             | **50 m**            | 1,00 €/m      | 50 €       |
| 3G2,5   | 45 m             | **55 m**            | 1,80 €/m      | 99 €       |
| 3G6     | 3 m              | **10 m**            | 4,50 €/m      | 45 €       |
| 3G10    | 3 m              | **10 m**            | 4,00 €/m      | 40 €       |
|         |                  |                     |               | **234 €**  |

> Note : le 3G10 conserve une marge confortable pour raccordement/ajustements.

---

## Accessoires de raccordement (ordre de grandeur)

| Désignation                    | Quantité conseillée | Budget indicatif |
| ----------------------------- | ------------------- | ---------------- |
| Boîtes de dérivation étanches | 12 à 16             | 45-70 €          |
| Bornes Wago (mixte 1,5-6 mm²) | 1 lot (60 à 80)     | 45-70 €          |
| Gaines/protection passage combles | 1 lot           | 15-30 €          |
| Étiquettes/repérage           | 1 lot               | 10-15 €          |

Sous-total accessoires : **115-185 €**.

---

## Budget câblage consolidé (scénario sans sous-tableau)

- Câbles : **~234 €**
- Accessoires raccordement : **~115-185 €**
- **Total câblage estimé : 349-419 €**

Ce budget remplace l'ancien scénario incluant le remplacement d'un coffret divisionnaire étage.

---

## Points de vigilance chantier

- Vérifier la faisabilité réelle des 10 m sur chaque circuit avant coupe.
- Contrôler la protection mécanique au passage en combles.
- Soigner le repérage des 6 circuits étage dès le tirage.
- Mettre à jour les longueurs réelles après pose dans la documentation finale.

---

**Auteur** : GitHub Copilot
**Date** : 17 février 2026
**Version** : 5.0 - scénario tableau principal unique (sans sous-tableau étage)
