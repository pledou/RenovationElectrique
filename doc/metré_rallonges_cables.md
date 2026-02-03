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

| Circuit | Fonction | Section | Longueur rallonge | Quantité fils | Total linéaire |
|---------|----------|---------|-------------------|---------------|----------------|
| **Chaudière** | Chauffage | 2,5 mm² | 3,0 m | 3 fils (Ph+N+T) | 9,0 m |
| **L1** | Éclairage 1 | 1,5 mm² | 3,0 m | 3 fils (Ph+N+T) | 9,0 m |
| **L2** | Éclairage 2 | 1,5 mm² | 3,0 m | 3 fils (Ph+N+T) | 9,0 m |
| **P1** | Plaque cuisson | 6 mm² | 3,0 m | 3 fils (Ph+N+T) | 9,0 m |
| **P2** | Buanderie/Garage | 2,5 mm² | 3,0 m | 3 fils (Ph+N+T) | 9,0 m |
| **P3** | Séjour/Bureau/Four | 2,5 mm² | 3,0 m | 3 fils (Ph+N+T) | 9,0 m |
| **P4** | Cuisine | 2,5 mm² | 3,0 m | 3 fils (Ph+N+T) | 9,0 m |
| **sc_etage** | Alim sous-tableau | 6 mm² | 3,0 m | 3 fils (Ph+N+T) | 9,0 m |
| **sanitaire** | Chauffe-eau | 2,5 mm² | 3,0 m | 3 fils (Ph+N+T) | 9,0 m |

> **Note** : Le circuit onduleur solaire (optionnel) sera créé avec un câble neuf complet, pas de rallonge.

---

## Synthèse par Section de Câble

### Câble 1,5 mm² (H07V-U ou R)

| Circuit | Longueur | Total |
|---------|----------|-------|
| L1 (3 fils) | 3,0 m | 9,0 m |
| L2 (3 fils) | 3,0 m | 9,0 m |
| **TOTAL 1,5 mm²** | | **18 m** |

**À commander** : **20 m de câble 1,5 mm²** (marge 10%)

---

### Câble 2,5 mm² (H07V-U ou R)

| Circuit | Longueur | Total |
|---------|----------|-------|
| Chaudière (3 fils) | 3,0 m | 9,0 m |
| P2 (3 fils) | 3,0 m | 9,0 m |
| P3 (3 fils) | 3,0 m | 9,0 m |
| P4 (3 fils) | 3,0 m | 9,0 m |
| sanitaire (3 fils) | 3,0 m | 9,0 m |
| **TOTAL 2,5 mm²** | | **45 m** |

**À commander** : **50 m de câble 2,5 mm²** (marge 10%)

---

### Câble 6 mm² (H07V-U ou R)

| Circuit | Longueur | Total |
|---------|----------|-------|
| P1 - Plaque (3 fils) | 3,0 m | 9,0 m |
| sc_etage (3 fils) | 3,0 m | 9,0 m |
| **TOTAL 6 mm²** | | **18 m** |

**À commander** : **20 m de câble 6 mm²** (marge 10%)

---

## Récapitulatif des Achats

### Câbles électriques

| Section | Quantité | Prix unitaire | Total |
|---------|----------|---------------|-------|
| Câble 1,5 mm² H07V-U | 20 m | 0,80 €/m | 16 € |
| Câble 2,5 mm² H07V-U | 50 m | 1,20 €/m | 60 € |
| Câble 6 mm² H07V-U | 20 m | 2,50 €/m | 50 € |
| **TOTAL Câbles** | | | **126 €** |

### Accessoires de raccordement

| Quantité | Désignation | Prix unitaire | Total |
|----------|-------------|---------------|-------|
| 9 | Boîtes de dérivation étanche 100×100 mm | 3 € | 27 € |
| 27 | Bornes Wago 3 entrées 2,5-6 mm² | 1 € | 27 € |
| 1 | Rouleau adhésif isolant | 5 € | 5 € |
| 1 | Set étiquettes repérage | 8 € | 8 € |
| **TOTAL Accessoires** | | | **67 €** |

---

## Coût Total Rallonges

| Poste | Montant |
|-------|---------|
| Câbles électriques | 126 € |
| Accessoires raccordement | 67 € |
| **TOTAL** | **193 €** |

> **Note** : Ce coût remplace l'estimation initiale de 95 € qui était sous-évaluée. Le coût réel est plus élevé car :
> - 9 circuits à rallonger (pas 8)
> - Longueur de 3m par circuit (pas 2-2,5m)
> - Accessoires de raccordement complets

---

## Mise à Jour du Budget Global

| Poste | Montant initial | Montant réel |
|-------|----------------|--------------|
| Fixation murale | 20-30 € | 25 € |
| Goulotte | 60 € | 69 € |
| **Rallonges câbles** | **95 €** | **193 €** |
| Accessoires divers | - | 10 € |
| **TOTAL** | **175-185 €** | **297 €** |

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

### Option C : Alternative câbles en gaine
Utiliser du câble multiconducteur gainé (type RO2V) au lieu de fils séparés :
- Câble 3G1,5 mm² : ~1,00 €/m
- Câble 3G2,5 mm² : ~1,80 €/m
- Câble 3G6 mm² : ~4,50 €/m

**Coût avec câbles multiconducteurs** : ~140 € (économie de 13 €, mais installation légèrement plus complexe)

---

## Recommandation

**Procéder avec** :
1. Vérifier la longueur réelle des câbles existants (certains peuvent peut-être être réutilisés)
2. Acheter des bobines complètes pour réduire les coûts
3. Prévoir budget réaliste de **280-300 €** pour l'Option 3

**Comparaison finale Options 1 vs 3** :

| Critère | Option 1 (au-dessus ECS) | Option 3 (garage) |
|---------|--------------------------|-------------------|
| Coût rallonges | ~100 € (2m/circuit) | ~193 € (3m/circuit) |
| Coût total | ~165 € | ~300 € |
| Ergonomie | Moyenne (haute) | Excellente (idéale) |
| Conformité Consuel | Bonne | Optimale |

**Décision à prendre** :
- Si budget serré : **Option 1** reste valide et conforme
- Si validation Consuel prioritaire : **Option 3** recommandée (+135 €)

---

**Auteur** : GitHub Copilot  
**Date** : 3 février 2026  
**Version** : 1.0
