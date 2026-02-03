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

| Section | Circuits | Longueur/circuit | Total | Prix €/m | Total |
|---------|----------|------------------|-------|----------|-------|
| **3G1,5 mm²** | L1, L2 | 3,0 m | 6 m | 1,00 | 6 € |
| **3G2,5 mm²** | Chaudière, P2, P3, P4, sanitaire | 3,0 m | 15 m | 1,80 | 27 € |
| **3G6 mm²** | P1, sc_etage | 3,0 m | 6 m | 4,50 | 27 € |

**À commander** :
- **10 m de 3G1,5 mm²** (marge 40%) : **10 €**
- **20 m de 3G2,5 mm²** (marge 33%) : **36 €**
- **10 m de 3G6 mm²** (marge 40%) : **45 €**

**Total câbles : 91 €** (au lieu de 126 €) = **Économie de 35 €**

### Outillage nécessaire

| Outil | Usage | Prix | Note |
|-------|-------|------|------|
| **Pince à dénuder automatique** | Dénudage gaine + fils | 15-25 € | Indispensable |
| **Couteau d'électricien** | Incision gaine extérieure | 8-12 € | Recommandé |
| **Pince coupante de côté** | Coupe câbles | 10-15 € | Si non possédé |
| **Total outillage** | | **~35-50 €** | Investissement durable |

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

| Poste | Montant |
|-------|---------|
| Câbles multiconducteurs RO2V | 91 € |
| Accessoires raccordement | 67 € |
| Fixation tableau | 25 € |
| Goulotte | 69 € |
| **Outillage (pince + couteau)** | **40 €** |
| Accessoires divers | 10 € |
| **TOTAL** | **302 €** |

> **Note** : L'outillage (40 €) est un investissement permanent, pas un consommable. Hors outillage, le coût est de **262 €**.

---

## Procéder avec

**Comparaison finale Options 1 vs 3** (avec câbles multiconducteurs) :

| Critère | Option 1 (au-dessus ECS) | Option 3 (garage) |
|---------|--------------------------|-------------------|
| Coût câbles | ~75 € (2m/circuit) | ~91 € (3m/circuit) |
| Coût total (hors outillage) | ~145 € | ~262 € |
| Coût total (avec outillage) | ~185 € | ~302 € |
| Ergonomie | Moyenne (haute) | Excellente (idéale) |
| Conformité Consuel | Bonne | Optimale |

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

**Auteur** : GitHub Copilot  
**Date** : 3 février 2026  
**Version** : 2.0 - Avec câbles multiconducteurs
---

**Auteur** : GitHub Copilot  
**Date** : 3 février 2026  
**Version** : 1.0
