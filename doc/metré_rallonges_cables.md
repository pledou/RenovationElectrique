# Métré des Rallonges de Câbles

## Date
3 février 2026

## ✅ Options Retenues

- **Emplacement tableau RdC** : Garage, hauteur 110-150 cm (entrée haute ~150 cm)
- **Type de câbles** : Multiconducteurs RO2V (3G1,5 / 3G2,5 / 3G6 / 3G10 mm²)
- **Emplacement sous-tableau étage** : Hauteur 170-180 cm (descente depuis plafond à 250 cm)

> **Avantages câbles multiconducteurs** : Installation plus propre, meilleure protection mécanique, passage plus facile dans goulotte, aspect professionnel.

---

## Configuration

### Positions
- **Tableau actuel** : Au plafond buanderie (~210 cm de hauteur)
- **Circuits existants** : Arrivent par le plafond
- **Nouveau tableau** : Garage, hauteur 110-150 cm (entrée haute à ~150 cm)
- **Décalage horizontal** : 160 cm
- **Hauteur descente garage** : ~80 cm (du plafond 230 cm à entrée tableau 150 cm)

### Parcours type d'une rallonge
```
Tableau actuel (210 cm) 
    ↓ 0 cm (déjà au plafond)
    → 160 cm (horizontal dans goulotte plafond)
    ↓ Passage par-dessus mur (0 cm supplémentaire, déjà au bon niveau)
    ↓ 80 cm (descente garage jusqu'à entrée tableau 150 cm)
    + 60 cm (marge sécurité + raccordement dans boîtes de dérivation)
    
TOTAL par circuit : ~300 cm = 3,0 m
```

---

## Calcul Détaillé par Circuit

### Circuits à rallonger (8 circuits du RdC)

| Circuit       | Fonction           | Section | Longueur rallonge | Quantité fils   | Total linéaire |
| ------------- | ------------------ | ------- | ----------------- | --------------- | -------------- |
| **Chaudière** | Chauffage          | 2,5 mm² | 3,0 m             | 3 fils (Ph+N+T) | 9,0 m          |
| **L1**        | Éclairage 1        | 1,5 mm² | 3,0 m             | 3 fils (Ph+N+T) | 9,0 m          |
| **L2**        | Éclairage 2        | 1,5 mm² | 3,0 m             | 3 fils (Ph+N+T) | 9,0 m          |
| **P1**        | Plaque cuisson     | 6 mm²   | 3,0 m             | 3 fils (Ph+N+T) | 9,0 m          |
| **P2**        | Buanderie/Garage   | 2,5 mm² | 3,0 m             | 3 fils (Ph+N+T) | 9,0 m          |
| **P3**        | Séjour/Bureau/Four | 2,5 mm² | 3,0 m             | 3 fils (Ph+N+T) | 9,0 m          |
| **P4**        | Cuisine            | 2,5 mm² | 3,0 m             | 3 fils (Ph+N+T) | 9,0 m          |
| **sc_etage**  | Alim sous-tableau  | 6 mm²   | 3,0 m             | 3 fils (Ph+N+T) | 9,0 m          |
| **sanitaire** | Chauffe-eau        | 2,5 mm² | 3,0 m             | 3 fils (Ph+N+T) | 9,0 m          |

### Câble d'alimentation principale du tableau

| Câble                     | Section | Longueur | Quantité fils   | Total linéaire |
| ------------------------- | ------- | -------- | --------------- | -------------- |
| **Arrivée EDF → Tableau** | 10 mm²  | 3,0 m    | 3 fils (Ph+N+T) | 9,0 m          |

### Rallonge sous-tableau étage

| Câble                                        | Section | Longueur | Quantité fils   | Total linéaire |
| -------------------------------------------- | ------- | -------- | --------------- | -------------- |
| **Alimentation sous-tableau** (descente mur) | 6 mm²   | 1,0 m    | 3 fils (Ph+N+T) | 3,0 m          |

> **Note sous-tableau** : Rallonge nécessaire pour descendre le tableau du plafond (250 cm) à hauteur réglementaire (175 cm).

> **Note onduleur** : Le circuit onduleur solaire (optionnel) sera créé avec un câble neuf complet, pas de rallonge.

---

## Synthèse par Section de Câble

### Câble 3G1,5 mm² (RO2V multiconducteur)

| Circuit           | Longueur | Total   |
| ----------------- | -------- | ------- |
| L1                | 3,0 m    | 3,0 m   |
| L2                | 3,0 m    | 3,0 m   |
| **TOTAL RdC**     |          | **6 m** |

**À commander pour RdC** : **6 m** (pour tableau RdC uniquement, voir synthèse globale ci-dessous)

---

### Câble 3G2,5 mm² (RO2V multiconducteur)

| Circuit   | Longueur | Total    |
| --------- | -------- | -------- |
| Chaudière | 3,0 m    | 3,0 m    |
| P2        | 3,0 m    | 3,0 m    |
| P3        | 3,0 m    | 3,0 m    |
| P4        | 3,0 m    | 3,0 m    |
| sanitaire | 3,0 m    | 3,0 m    |
| **TOTAL RdC** |      | **15 m** |

**À commander pour RdC** : **15 m** (pour tableau RdC uniquement, voir synthèse globale ci-dessous)

---

### Câble 3G6 mm² (RO2V multiconducteur)

| Circuit                                | Longueur | Total   |
| -------------------------------------- | -------- | ------- |
| P1 - Plaque                            | 3,0 m    | 3,0 m   |
| sc_etage - Rallonge tableau RdC        | 3,0 m    | 3,0 m   |
| sc_etage - Rallonge sous-tableau étage | 1,0 m    | 1,0 m   |
| **TOTAL**                              |          | **7 m** |

**À commander** : **10 m** (marge ~40%, voir liste de courses ci-dessous)

---

### Câble 3G10 mm² (RO2V multiconducteur)

| Circuit               | Longueur | Total   |
| --------------------- | -------- | ------- |
| Arrivée EDF → Tableau | 3,0 m    | 3,0 m   |
| **TOTAL**             |          | **3 m** |

**À commander** : **10 m** (marge confortable, voir liste de courses ci-dessous)

> **Note importante** : Section 10 mm² adaptée pour abonnement 9-12 kVA (45-60A). Si abonnement > 12 kVA, prévoir du 16 mm².

---

## Métré Rallonges Sous-Tableau Étage

### Configuration sous-tableau

**Position actuelle** : Plafond étage (~250 cm)
**Position future** : Hauteur 170-180 cm (pour sécurité enfants)
**Descente nécessaire** : 70-80 cm par circuit
**Marge raccordement** : 20-30 cm

### Parcours type rallonge sous-tableau
```
Position actuelle (250 cm plafond)
    ↓ 70-80 cm (descente vers tableau à 170-180 cm)
    + 20-30 cm (marge sécurité + raccordement)
    
TOTAL par circuit : 90-110 cm ≈ 1,0 m
```

### Circuits à rallonger (6 circuits étage)

| Circuit | Fonction         | Section | Longueur rallonge | Quantité fils   | Total linéaire |
| ------- | ---------------- | ------- | ----------------- | --------------- | -------------- |
| **VMI** | Ventilation      | 1,5 mm² | 1,0 m             | 3 fils (Ph+N+T) | 3,0 m          |
| **P5**  | Prises étage     | 2,5 mm² | 1,0 m             | 3 fils (Ph+N+T) | 3,0 m          |
| **L3**  | Éclairage étage  | 1,5 mm² | 1,0 m             | 3 fils (Ph+N+T) | 3,0 m          |
| **L4**  | Éclairage SdB    | 1,5 mm² | 1,0 m             | 3 fils (Ph+N+T) | 3,0 m          |
| **P6**  | Prises chambre 3 | 2,5 mm² | 1,0 m             | 3 fils (Ph+N+T) | 3,0 m          |
| **P7**  | Prise palier     | 2,5 mm² | 1,0 m             | 3 fils (Ph+N+T) | 3,0 m          |

---

### Synthèse par section - Sous-tableau étage

#### Câble 3G1,5 mm² (éclairages + VMI)

| Circuit           | Longueur | Total   |
| ----------------- | -------- | ------- |
| VMI               | 1,0 m    | 1,0 m   |
| L3                | 1,0 m    | 1,0 m   |
| L4                | 1,0 m    | 1,0 m   |
| **TOTAL Étage**   |          | **3 m** |

**À commander pour étage** : **3 m** (voir synthèse globale ci-dessous)

#### Câble 3G2,5 mm² (prises)

| Circuit         | Longueur | Total   |
| --------------- | -------- | ------- |
| P5              | 1,0 m    | 1,0 m   |
| P6              | 1,0 m    | 1,0 m   |
| P7              | 1,0 m    | 1,0 m   |
| **TOTAL Étage** |          | **3 m** |

**À commander pour étage** : **3 m** (voir synthèse globale ci-dessous)

---

## � Synthèse Globale des Câbles (RdC + Étage)

### Récapitulatif par section

| Section        | Tableau RdC | Sous-tableau Étage | **Total nécessaire** | **À commander** | Prix unitaire | **Total** |
| -------------- | ----------- | ------------------ | -------------------- | --------------- | ------------- | --------- |
| **3G1,5 mm²**  | 6 m         | 3 m                | **9 m**              | **15 m**        | 1,00 €/m      | **15 €**  |
| **3G2,5 mm²**  | 15 m        | 3 m                | **18 m**             | **25 m**        | 1,80 €/m      | **45 €**  |
| **3G6 mm²**    | 7 m         | -                  | **7 m**              | **10 m**        | 4,50 €/m      | **45 €**  |
| **3G10 mm²**   | 3 m         | -                  | **3 m**              | **10 m**        | 4,00 €/m      | **40 €**  |
| **TOTAL**      |             |                    |                      |                 |               | **145 €** |

> **Note marges** : Les marges permettent d'avoir du câble de réserve pour les raccordements et imprévus (40-50% pour sections > 6mm², 35-40% pour petites sections).

---

## �📋 LISTE DE COURSES COMPLÈTE ET SIMPLIFIÉE

### ✅ Câbles électriques (multiconducteurs RO2V)

- [ ] **15 mètres** de câble RO2V **3G1,5 mm²** → **15 €**
- [ ] **25 mètres** de câble RO2V **3G2,5 mm²** → **45 €**
- [ ] **10 mètres** de câble RO2V **3G6 mm²** → **45 €**
- [ ] **10 mètres** de câble RO2V **3G10 mm²** (alimentation principale tableau) → **40 €**

**Sous-total câbles : 145 €**

### ✅ Accessoires de raccordement

- [ ] **9 boîtes** de dérivation étanche **100×100 mm** (tableau RdC) → **27 €**
- [ ] **6 boîtes** de dérivation **80×80 mm** (sous-tableau étage) → **15 €**
- [ ] **50 bornes Wago** (lot mixte 2,5-6mm² et 1,5-2,5mm²) → **45 €**
  - *Détail : 27 bornes 3 entrées 2,5-6mm² + 18 bornes 3 entrées 1,5-2,5mm²*
- [ ] **1 rouleau** adhésif isolant → **5 €**
- [ ] **2 sets** d'étiquettes repérage → **11 €**

**Sous-total accessoires : 103 €**

### ✅ Tableaux électriques

- [ ] **1 Coffret 3 rangées de 13 modules avec porte** (tableau principal RdC) - Schneider Rési9 ou équivalent → **80 €**
- [ ] **1 Coffret 13 modules avec porte** (sous-tableau étage) - Schneider Rési9 ou équivalent → **65 €**

**Sous-total tableaux : 145 €**

### ✅ Goulotte et fixation (tableau RdC uniquement)

- [ ] **4 mètres** goulotte 80×40 mm PVC blanc → **40 €**
- [ ] **4 angles** plat 90° → **12 €**
- [ ] **2 embouts** entrée goulotte → **4 €**
- [ ] **25 fixations** + chevilles → **13 €**
- [ ] **4 chevilles** métal M8 (fixation tableau) → **8 €**
- [ ] Vis et accessoires fixation tableau → **10 €**
- [ ] Support tableau (si nécessaire) → **7 €**
- [ ] Accessoires divers → **10 €**

**Sous-total goulotte/fixation : 104 €**

### ✅ Outillage (si non possédé)

- [ ] Pince à dénuder automatique (Knipex ou équivalent) → **25 €**
- [ ] Couteau d'électricien → **10 €**
- [ ] Pince coupante de côté (si besoin) → **15 €**

**Sous-total outillage : 50 €** *(optionnel si déjà en possession)*

---

### 💳 BUDGET COURSES TOTAL

| Catégorie                    | Montant   |
| ---------------------------- | --------- |
| **Tableaux électriques**     | **145 €** |
| **Câbles électriques**       | **145 €** |
| **Accessoires raccordement** | **103 €** |
| **Goulotte et fixation**     | **104 €** |
| **Outillage** (optionnel)    | **50 €**  |
| **TOTAL SANS OUTILLAGE**     | **497 €** |
| **TOTAL AVEC OUTILLAGE**     | **547 €** |

---

**Auteur** : GitHub Copilot  
**Date** : 4 février 2026  
**Version** : 4.0 - Synthèse cohérente avec câbles multiconducteurs RO2V
