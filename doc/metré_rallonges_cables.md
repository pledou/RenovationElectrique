# Métré des Rallonges de Câbles

## Date
3 février 2026

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

### Câble 1,5 mm² (H07V-U ou R)

| Circuit           | Longueur | Total    |
| ----------------- | -------- | -------- |
| L1 (3 fils)       | 3,0 m    | 9,0 m    |
| L2 (3 fils)       | 3,0 m    | 9,0 m    |
| **TOTAL 1,5 mm²** |          | **18 m** |

**À commander** : **20 m de câble 1,5 mm²** (marge 10%)

---

### Câble 2,5 mm² (H07V-U ou R)

| Circuit            | Longueur | Total    |
| ------------------ | -------- | -------- |
| Chaudière (3 fils) | 3,0 m    | 9,0 m    |
| P2 (3 fils)        | 3,0 m    | 9,0 m    |
| P3 (3 fils)        | 3,0 m    | 9,0 m    |
| P4 (3 fils)        | 3,0 m    | 9,0 m    |
| sanitaire (3 fils) | 3,0 m    | 9,0 m    |
| **TOTAL 2,5 mm²**  |          | **45 m** |

**À commander** : **50 m de câble 2,5 mm²** (marge 10%)

---

### Câble 6 mm² (H07V-U ou R)

| Circuit                                         | Longueur | Total    |
| ----------------------------------------------- | -------- | -------- |
| P1 - Plaque (3 fils)                            | 3,0 m    | 9,0 m    |
| sc_etage - Rallonge tableau RdC (3 fils)        | 3,0 m    | 9,0 m    |
| sc_etage - Rallonge sous-tableau étage (3 fils) | 1,0 m    | 3,0 m    |
| **TOTAL 6 mm²**                                 |          | **21 m** |

**À commander** : **25 m de câble 6 mm²** (marge ~20%)

---

### Câble 10 mm² (H07V-U ou R)

| Circuit                        | Longueur | Total   |
| ------------------------------ | -------- | ------- |
| Arrivée EDF → Tableau (3 fils) | 3,0 m    | 9,0 m   |
| **TOTAL 10 mm²**               |          | **9 m** |

**À commander** : **10 m de câble 10 mm²** (marge 10%)

> **Note importante** : Section 10 mm² adaptée pour abonnement 9-12 kVA (45-60A). Si abonnement > 12 kVA, prévoir du 16 mm².

---

## Récapitulatif des Achats

### Câbles électriques

| Section              | Quantité | Prix unitaire | Total     |
| -------------------- | -------- | ------------- | --------- |
| Câble 1,5 mm² H07V-U | 20 m     | 0,80 €/m      | 16 €      |
| Câble 2,5 mm² H07V-U | 50 m     | 1,20 €/m      | 60 €      |
| Câble 6 mm² H07V-U   | 25 m     | 2,50 €/m      | 63 €      |
| Câble 10 mm² H07V-U  | 10 m     | 4,00 €/m      | 40 €      |
| **TOTAL Câbles**     |          |               | **179 €** |

### Accessoires de raccordement

| Quantité              | Désignation                             | Prix unitaire | Total    |
| --------------------- | --------------------------------------- | ------------- | -------- |
| 9                     | Boîtes de dérivation étanche 100×100 mm | 3 €           | 27 €     |
| 27                    | Bornes Wago 3 entrées 2,5-6 mm²         | 1 €           | 27 €     |
| 1                     | Rouleau adhésif isolant                 | 5 €           | 5 €      |
| 1                     | Set étiquettes repérage                 | 8 €           | 8 €      |
| **TOTAL Accessoires** |                                         |               | **67 €** |

---

## Coût Total Rallonges

| Poste                    | Montant   |
| ------------------------ | --------- |
| Câbles électriques       | 126 €     |
| Accessoires raccordement | 67 €      |
| **TOTAL**                | **193 €** |

> **Note** : Ce coût remplace l'estimation initiale de 95 € qui était sous-évaluée. Le coût réel est plus élevé car :
> - 9 circuits à rallonger (pas 8)
> - Longueur de 3m par circuit (pas 2-2,5m)
> - Accessoires de raccordement complets

---

## Mise à Jour du Budget Global

| Poste                | Montant initial | Montant réel |
| -------------------- | --------------- | ------------ |
| Fixation murale      | 20-30 €         | 25 €         |
| Goulotte             | 60 €            | 69 €         |
| **Rallonges câbles** | **95 €**        | **193 €**    |
| Accessoires divers   | -               | 10 €         |
| **TOTAL**            | **175-185 €**   | **297 €**    |

### ⚠️ Surcoût identifié : +110 €

Le budget initial était sous-estimé. Le coût réaliste pour l'Option 3 (garage) est de **~300 €** au lieu de 175-185 €.

---

## Options de Réduction des Coûts

### Option A : Réutiliser les câbles existants
Si les câbles actuels sont en bon état et suffisamment longs, il est possible de :
- Démonter les câbles de l'ancien tableau
- Vérifier leur longueur effective
- Les prolonger uniquement si nécessaire

**Économie potentielle** : 50-100 € (selon câbles réutilisables)

### Option B : Acheter en bobines complètes
Les prix indiqués sont au détail. L'achat en bobines de 25-50m peut réduire le coût :
- Bobine 50m câble 2,5 mm² : ~45 € au lieu de 60 €
- Bobine 25m câble 1,5 mm² : ~12 € au lieu de 16 €

**Économie potentielle** : 15-20 €

### ✅ Option C : Câbles multiconducteurs (RECOMMANDÉE)

**Solution choisie** : Utiliser du câble multiconducteur gainé (type RO2V) au lieu de fils séparés.

**Avantages** :
- ✅ Installation plus propre et plus rapide
- ✅ Meilleure protection mécanique (gaine extérieure)
- ✅ Pas de risque d'inversion de fils
- ✅ Passage plus facile dans la goulotte
- ✅ Aspect professionnel

**Difficulté** : **Faible** 
- Dénudage simple avec outil adapté
- Technique de base en électricité
- Vidéos tutoriels disponibles en ligne

**Type de câbles** :
- Câble 3G1,5 mm² (Ph+N+T) : ~1,00 €/m
- Câble 3G2,5 mm² (Ph+N+T) : ~1,80 €/m
- Câble 3G6 mm² (Ph+N+T) : ~4,50 €/m

**Coût avec câbles multiconducteurs** : ~140 € (économie de 13 € vs fils séparés)

---

## ✅ Solution Retenue : Câbles Multiconducteurs

### Métré avec câbles RO2V

| Section       | Circuits                         | Longueur/circuit | Total | Prix €/m | Total |
| ------------- | -------------------------------- | ---------------- | ----- | -------- | ----- |
| **3G1,5 mm²** | L1, L2                           | 3,0 m            | 6 m   | 1,00     | 6 €   |
| **3G2,5 mm²** | Chaudière, P2, P3, P4, sanitaire | 3,0 m            | 15 m  | 1,80     | 27 €  |
| **3G6 mm²**   | P1, sc_etage                     | 3,0 m            | 6 m   | 4,50     | 27 €  |

**À commander** :
- **10 m de 3G1,5 mm²** (marge 40%) : **10 €**
- **20 m de 3G2,5 mm²** (marge 33%) : **36 €**
- **10 m de 3G6 mm²** (marge 40%) : **45 €**

**Total câbles : 91 €** (au lieu de 126 €) = **Économie de 35 €**

### Outillage nécessaire

| Outil                           | Usage                     | Prix         | Note                   |
| ------------------------------- | ------------------------- | ------------ | ---------------------- |
| **Pince à dénuder automatique** | Dénudage gaine + fils     | 15-25 €      | Indispensable          |
| **Couteau d'électricien**       | Incision gaine extérieure | 8-12 €       | Recommandé             |
| **Pince coupante de côté**      | Coupe câbles              | 10-15 €      | Si non possédé         |
| **Total outillage**             |                           | **~35-50 €** | Investissement durable |

> **💡 Astuce** : Ces outils serviront pour tous vos futurs travaux électriques. Investissement rentabilisé dès la première utilisation.

### Technique de dénudage (câble multiconducteur)

**Étape 1 : Dénuder la gaine extérieure**
1. Inciser la gaine sur 5-8 cm avec couteau d'électricien
2. Attention à ne pas entailler les conducteurs internes
3. Retirer la gaine extérieure

**Étape 2 : Dénuder les conducteurs**
1. Utiliser la pince à dénuder automatique (réglage selon section)
2. Dénuder 10-12 mm pour raccordement Wago
3. Respecter les couleurs : Bleu=Neutre, Vert/Jaune=Terre, autre=Phase

**Difficulté** : ⭐⭐☆☆☆ (2/5 - Facile avec bon outil)
**Temps** : ~2 min par raccordement une fois la technique maîtrisée

### Recommandation produits

**Câbles** (norme NF, marquage CE) :
- Nexans ou Lafarge (qualité pro)
- Disponible en GSB (Leroy Merlin, Castorama) ou magasins spécialisés

**Pince à dénuder recommandée** :
- Knipex 12 40 200 (~25 €) - référence professionnelle
- Ou équivalent Stanley, Facom (15-20 €)

---

## Budget Final Révisé avec Multiconducteurs

| Poste                           | Montant   |
| ------------------------------- | --------- |
| Câbles multiconducteurs RO2V    | 91 €      |
| Accessoires raccordement        | 67 €      |
| Fixation tableau                | 25 €      |
| Goulotte                        | 69 €      |
| **Outillage (pince + couteau)** | **40 €**  |
| Accessoires divers              | 10 €      |
| **TOTAL**                       | **302 €** |

> **Note** : L'outillage (40 €) est un investissement permanent, pas un consommable. Hors outillage, le coût est de **262 €**.

---

## Procéder avec

**Comparaison finale Options 1 vs 3** (avec câbles multiconducteurs) :

| Critère                     | Option 1 (au-dessus ECS) | Option 3 (garage)   |
| --------------------------- | ------------------------ | ------------------- |
| Coût câbles                 | ~75 € (2m/circuit)       | ~91 € (3m/circuit)  |
| Coût total (hors outillage) | ~145 €                   | ~262 €              |
| Coût total (avec outillage) | ~185 €                   | ~302 €              |
| Ergonomie                   | Moyenne (haute)          | Excellente (idéale) |
| Conformité Consuel          | Bonne                    | Optimale            |

**✅ Décision validée avec multiconducteurs** :
- **Option 3 (garage)** : ~262 € (hors outillage) ou 302 € (avec outillage)
- Installation professionnelle et durable
- Outillage réutilisable pour futurs travaux
- Câbles multiconducteurs plus faciles à installer
## Liste de Courses Finale

### Câbles électriques
- [ ] 10 m de câble RO2V 3G1,5 mm² (~10 €)
- [ ] 20 m de câble RO2V 3G2,5 mm² (~36 €)
- [ ] 10 m de câble RO2V 3G6 mm² (~45 €)

### Accessoires
- [ ] 9 boîtes de dérivation étanche 100×100 mm (~27 €)
- [ ] 27 bornes Wago 3 entrées 2,5-6 mm² (~27 €)
- [ ] 1 rouleau adhésif isolant (~5 €)
- [ ] 1 set étiquettes repérage (~8 €)

### Goulotte
- [ ] 4 m goulotte 80×40 mm PVC blanc (~40 €)
- [ ] 4 angles plat 90° (~12 €)
- [ ] 2 embouts entrée goulotte (~4 €)
- [ ] 25 fixations + chevilles (~13 €)

### Fixation tableau
- [ ] 4 chevilles métal M8 (~8 €)
- [ ] Vis et accessoires fixation (~10 €)
- [ ] Support tableau (si nécessaire) (~7 €)

### Outillage (si non possédé)
- [ ] Pince à dénuder automatique (~25 €)
- [ ] Couteau d'électricien (~10 €)
- [ ] Pince coupante (si besoin) (~15 €)

**Budget total : 262 € (hors outillage) ou 302 € (avec outillage)**

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

#### Câble 1,5 mm² (éclairages + VMI)

| Circuit           | Longueur | Total   |
| ----------------- | -------- | ------- |
| VMI (3 fils)      | 1,0 m    | 3,0 m   |
| L3 (3 fils)       | 1,0 m    | 3,0 m   |
| L4 (3 fils)       | 1,0 m    | 3,0 m   |
| **TOTAL 1,5 mm²** |          | **9 m** |

**À commander** : **10 m de câble 1,5 mm²** (marge 10%)

#### Câble 2,5 mm² (prises)

| Circuit           | Longueur | Total   |
| ----------------- | -------- | ------- |
| P5 (3 fils)       | 1,0 m    | 3,0 m   |
| P6 (3 fils)       | 1,0 m    | 3,0 m   |
| P7 (3 fils)       | 1,0 m    | 3,0 m   |
| **TOTAL 2,5 mm²** |          | **9 m** |

**À commander** : **10 m de câble 2,5 mm²** (marge 10%)

---

### Coût rallonges sous-tableau étage

#### Option câbles séparés (H07V-U)

| Section              | Quantité | Prix unitaire | Total    |
| -------------------- | -------- | ------------- | -------- |
| Câble 1,5 mm² H07V-U | 10 m     | 0,80 €/m      | 8 €      |
| Câble 2,5 mm² H07V-U | 10 m     | 1,20 €/m      | 12 €     |
| **TOTAL Câbles**     |          |               | **20 €** |

#### Option câbles multiconducteurs (RO2V) - ✅ RECOMMANDÉE

| Section                           | Quantité | Prix €/m | Total    |
| --------------------------------- | -------- | -------- | -------- |
| Câble 3G1,5 mm² (VMI, L3, L4)     | 3 m      | 1,00     | 3 €      |
| Câble 3G2,5 mm² (P5, P6, P7)      | 3 m      | 1,80     | 5 €      |
| Marge 50%                         | 3 m      | -        | 4 €      |
| **TOTAL Câbles multiconducteurs** |          |          | **12 €** |

#### Accessoires de raccordement

| Quantité              | Désignation                       | Prix unitaire | Total    |
| --------------------- | --------------------------------- | ------------- | -------- |
| 6                     | Boîtes de dérivation 80×80 mm     | 2,50 €        | 15 €     |
| 18                    | Bornes Wago 3 entrées 1,5-2,5 mm² | 0,80 €        | 14 €     |
| 1                     | Set étiquettes repérage           | 3 €           | 3 €      |
| **TOTAL Accessoires** |                                   |               | **32 €** |

---

### Budget total sous-tableau étage (rallonges uniquement)

| Poste                    | Montant câbles séparés | Montant multiconducteurs |
| ------------------------ | ---------------------- | ------------------------ |
| Câbles                   | 20 €                   | 12 €                     |
| Accessoires raccordement | 32 €                   | 32 €                     |
| **TOTAL**                | **52 €**               | **44 €**                 |

> **💡 Recommandation** : Utiliser les câbles multiconducteurs RO2V pour une installation plus professionnelle et plus rapide (économie de 8 € + gain de temps).

---

### Comparaison totale avec métré initial

**Estimation initiale** : 30-60 € (pour 1,00-1,50m par circuit)
**Métré réaliste** : 44-52 € (pour 0,70-1,00m par circuit avec multiconducteurs)

✅ **Budget conforme** : La rallonge moindre (70-80cm vs 100-150cm) compense les coûts accessoires.

---

## 📦 SYNTHÈSE GLOBALE DES ACHATS (Tableau Principal + Sous-Tableau)

### Total câbles nécessaires

#### Câble 3G1,5 mm² (multiconducteur)

| Localisation           | Circuits    | Longueur unitaire | Quantité circuits | Total    |
| ---------------------- | ----------- | ----------------- | ----------------- | -------- |
| **Tableau RdC**        | L1, L2      | 3,0 m             | 2                 | 6 m      |
| **Sous-tableau étage** | VMI, L3, L4 | 1,0 m             | 3                 | 3 m      |
| **SOUS-TOTAL**         |             |                   |                   | **9 m**  |
| **+ Marge 40%**        |             |                   |                   | **4 m**  |
| **TOTAL À COMMANDER**  |             |                   |                   | **15 m** |

**Prix** : 15 m × 1,00 €/m = **15 €**

---

#### Câble 3G2,5 mm² (multiconducteur)

| Localisation           | Circuits                         | Longueur unitaire | Quantité circuits | Total    |
| ---------------------- | -------------------------------- | ----------------- | ----------------- | -------- |
| **Tableau RdC**        | Chaudière, P2, P3, P4, sanitaire | 3,0 m             | 5                 | 15 m     |
| **Sous-tableau étage** | P5, P6, P7                       | 1,0 m             | 3                 | 3 m      |
| **SOUS-TOTAL**         |                                  |                   |                   | **18 m** |
| **+ Marge 35%**        |                                  |                   |                   | **7 m**  |
| **TOTAL À COMMANDER**  |                                  |                   |                   | **25 m** |

**Prix** : 25 m × 1,80 €/m = **45 €**

---

#### Câble 3G6 mm² (multiconducteur)

| Localisation           | Circuits              | Longueur unitaire | Quantité circuits | Total    |
| ---------------------- | --------------------- | ----------------- | ----------------- | -------- |
| **Tableau RdC**        | P1 (plaque), sc_etage | 3,0 m             | 2                 | 6 m      |
| **Sous-tableau étage** | -                     | -                 | 0                 | 0 m      |
| **SOUS-TOTAL**         |                       |                   |                   | **6 m**  |
| **+ Marge 40%**        |                       |                   |                   | **3 m**  |
| **TOTAL À COMMANDER**  |                       |                   |                   | **10 m** |

**Prix** : 10 m × 4,50 €/m = **45 €**

---

### Total accessoires consolidé

#### Boîtes de dérivation

| Localisation           | Quantité | Taille     | Prix unitaire | Total    |
| ---------------------- | -------- | ---------- | ------------- | -------- |
| **Tableau RdC**        | 9        | 100×100 mm | 3,00 €        | 27 €     |
| **Sous-tableau étage** | 6        | 80×80 mm   | 2,50 €        | 15 €     |
| **TOTAL**              | **15**   |            |               | **42 €** |

#### Bornes Wago

| Localisation           | Quantité | Type                  | Prix unitaire | Total    |
| ---------------------- | -------- | --------------------- | ------------- | -------- |
| **Tableau RdC**        | 27       | 3 entrées 2,5-6 mm²   | 1,00 €        | 27 €     |
| **Sous-tableau étage** | 18       | 3 entrées 1,5-2,5 mm² | 0,80 €        | 14 €     |
| **TOTAL**              | **45**   |                       |               | **41 €** |

#### Autres accessoires

| Désignation                     | Quantité | Prix unitaire | Total    |
| ------------------------------- | -------- | ------------- | -------- |
| Rouleau adhésif isolant         | 1        | 5 €           | 5 €      |
| Set étiquettes repérage (RdC)   | 1        | 8 €           | 8 €      |
| Set étiquettes repérage (Étage) | 1        | 3 €           | 3 €      |
| **TOTAL Autres**                |          |               | **16 €** |

**TOTAL ACCESSOIRES** : 42 + 41 + 16 = **99 €**

---

### 🛒 RÉCAPITULATIF BUDGET TOTAL RALLONGES

| Poste                | Tableau RdC | Sous-tableau | **TOTAL PROJET** |
| -------------------- | ----------- | ------------ | ---------------- |
| **Câbles 3G1,5 mm²** | 10 €        | 5 €          | **15 €**         |
| **Câbles 3G2,5 mm²** | 36 €        | 9 €          | **45 €**         |
| **Câbles 3G6 mm²**   | 45 €        | -            | **45 €**         |
| **Accessoires**      | 67 €        | 32 €         | **99 €**         |
| **SOUS-TOTAL**       | **158 €**   | **46 €**     | **204 €**        |

### Autres postes (tableau RdC uniquement)

| Poste                   | Montant   |
| ----------------------- | --------- |
| Fixation murale tableau | 25 €      |
| Goulotte                | 69 €      |
| Accessoires divers      | 10 €      |
| **SOUS-TOTAL Autres**   | **104 €** |

### 💰 BUDGET TOTAL GLOBAL

| Catégorie                          | Montant   |
| ---------------------------------- | --------- |
| **Rallonges câbles (RdC + Étage)** | **204 €** |
| **Installation tableau RdC**       | **104 €** |
| **Outillage (si non possédé)**     | **40 €**  |
| **TOTAL HORS OUTILLAGE**           | **308 €** |
| **TOTAL AVEC OUTILLAGE**           | **348 €** |

> **💡 Note** : L'outillage (pince à dénuder 25 € + couteau 10 € + pince coupante 15 €) est un investissement permanent pour tous vos futurs travaux électriques.

---

## 📋 LISTE DE COURSES COMPLÈTE ET SIMPLIFIÉE

### ✅ Câbles électriques (multiconducteurs RO2V)

- [ ] **15 mètres** de câble RO2V **3G1,5 mm²** → **15 €**
- [ ] **25 mètres** de câble RO2V **3G2,5 mm²** → **45 €**
- [ ] **15 mètres** de câble RO2V **3G6 mm²** (dont 1m rallonge sous-tableau étage) → **63 €**
- [ ] **10 mètres** de câble RO2V **3G10 mm²** (alimentation principale tableau) → **40 €**

**Sous-total câbles : 163 €**

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
| **Câbles électriques**       | **163 €** |
| **Accessoires raccordement** | **103 €** |
| **Goulotte et fixation**     | **104 €** |
| **Outillage** (optionnel)    | **50 €**  |
| **TOTAL SANS OUTILLAGE**     | **515 €** |
| **TOTAL AVEC OUTILLAGE**     | **565 €** |

---

**Auteur** : GitHub Copilot  
**Date** : 3 février 2026  
**Version** : 3.0 - Avec sous-tableau étage et synthèse globale
