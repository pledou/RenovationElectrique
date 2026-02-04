# Plan d'Organisation Interne du Tableau Électrique

## Date
4 février 2026

## Référence
Basé sur [proposition_tableau_electrique.md](proposition_tableau_electrique.md)

---

## Configuration Générale

**Tableau** : Coffret 3 rangées × 13 modules (39 modules disponibles)
- **21 modules utilisés**
- **18 modules libres** (pour extensions futures)

**Localisation** : Garage, hauteur 110-150 cm (entrée haute ~150 cm)

---

## Vue d'Ensemble des Rangées

```
╔═══════════════════════════════════════════════════════════════╗
║               TABLEAU ÉLECTRIQUE PRINCIPAL - GARAGE           ║
║                    3 rangées × 13 modules                     ║
╠═══════════════════════════════════════════════════════════════╣
║ RANGÉE 1 │ Type A │ P1 │ P2 │ P4 │ LIBRE (8 modules)         ║
║          │  40A   │32A │20A │20A │                            ║
╠═══════════════════════════════════════════════════════════════╣
║ RANGÉE 2 │ Type AC│Chd │L1 │L2 │P3 │Ond│Mes│sc │LIBRE (3)   ║
║          │  40A   │20A │16A│16A│20A│20A│(2)│20A│             ║
╠═══════════════════════════════════════════════════════════════╣
║ RANGÉE 3 │ Type A │ ECS │ LIBRE (10 modules)                 ║
║          │  40A   │ 20A │                                     ║
╚═══════════════════════════════════════════════════════════════╝
```

**Légende** :
- Chd = Chaudière + domotique + routeur ECS
- L1/L2 = Éclairages
- P1-P4 = Prises
- Ond = Onduleur solaire
- Mes = Équipement mesure (2 modules)
- sc = Sous-compteur étage
- ECS = Chauffe-eau

---

## RANGÉE 1 - Circuits Prioritaires (30mA Type A)

### Schéma Détaillé

```
┌──────────────────────────────────────────────────────────────┐
│ Module │  1-2  │  3  │  4  │  5  │ 6 │ 7 │ 8 │ 9 │10 │11-13  │
├────────┼───────┼─────┼─────┼─────┼───┼───┼───┼───┼───┼───────┤
│ Type   │ DIFF  │ DJ  │ DJ  │ DJ  │   │   │   │   │   │ LIBRE │
│        │ 40A   │ 32A │ 20A │ 20A │   │   │   │   │   │       │
├────────┼───────┼─────┼─────┼─────┼───┼───┼───┼───┼───┼───────┤
│Circuit │Type A │ P1  │ P2  │ P4  │   │   │   │   │   │       │
│        │ ▓▓▓▓  │Plaqu│Buan│Cuis │   │   │   │   │   │       │
└────────┴───────┴─────┴─────┴─────┴───┴───┴───┴───┴───┴───────┘
         └──── Peigne d'alimentation horizontale ────────────────┘
```

### Détail des connexions

| Module | Équipement                | Type            | Circuit                   | Section | Longueur | Notes                                 |
| ------ | ------------------------- | --------------- | ------------------------- | ------- | -------- | ------------------------------------- |
| 1-2    | Interrupteur différentiel | 40A 30mA Type A | -                         | -       | -        | Obligatoire pour plaque et lave-linge |
| 3      | Disjoncteur               | 32A             | **P1 - Plaque cuisson**   | 6 mm²   | 5m       | **Changer 10A→32A**                   |
| 4      | Disjoncteur               | 20A             | **P2 - Buanderie/Garage** | 2.5 mm² | 12m      | Lave-linge, sèche-linge               |
| 5      | Disjoncteur               | 20A             | **P4 - Prises cuisine**   | 2.5 mm² | 10m      | 3 prises                              |
| 6-13   | -                         | -               | **LIBRE**                 | -       | -        | 8 emplacements disponibles            |

**Charge maximale théorique** : 32A + 20A + 20A = 72A  
**Différentiel** : 40A adapté avec coefficient de diversité

### Câblage

**Arrivée alimentation** :
- Phase : Peigne horizontal depuis différentiel
- Neutre : Bornier de neutre (en haut)
- Terre : Bornier de terre (en bas)

**Repérage des câbles** :
- **P1** : Rouge (étiquette "Plaque cuisson")
- **P2** : Orange (étiquette "Buanderie/Garage")
- **P4** : Bleu (étiquette "Cuisine prises")

---

## RANGÉE 2 - Circuits Généraux (30mA Type AC)

### Schéma Détaillé

```
┌──────────────────────────────────────────────────────────────┐
│ Module │  1-2  │  3  │  4  │  5  │  6  │  7  │ 8-9 │ 10  │11-13│
├────────┼───────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┤
│ Type   │ DIFF  │ DJ  │ DJ  │ DJ  │ DJ  │ DJ  │Equip│ DJ  │LIBRE│
│        │ 40A   │ 20A │ 16A │ 16A │ 20A │ 20A │Mesu │ 20A │     │
├────────┼───────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┤
│Circuit │Type AC│Chaud│ L1  │ L2  │ P3  │Ondul│ (2) │sc_et│     │
│        │ ▓▓▓▓  │+Rou │Ecl1 │Ecl2 │Séj/ │solar│modul│ étag│     │
│        │       │ ECS │     │     │Four │     │  es │  e  │     │
└────────┴───────┴─────┴─────┴─────┴─────┴─────┴─────┴─────┴─────┘
         └──── Peigne d'alimentation horizontale ────────────────┘
```

### Détail des connexions

| Module | Équipement                | Type             | Circuit                          | Section | Longueur | Notes                      |
| ------ | ------------------------- | ---------------- | -------------------------------- | ------- | -------- | -------------------------- |
| 1-2    | Interrupteur différentiel | 40A 30mA Type AC | -                                | -       | -        | Circuits standards         |
| 3      | Disjoncteur               | 20A              | **Chaudière + routeur ECS**      | 2.5 mm² | 12m      | ESP + routeur solaire      |
| 4      | Disjoncteur               | 16A              | **L1 - Éclairage 1**             | 1.5 mm² | 15m      | Salon, garage, buanderie   |
| 5      | Disjoncteur               | 16A              | **L2 - Éclairage 2**             | 1.5 mm² | 10m      | Cuisine, entrée, WC        |
| 6      | Disjoncteur               | 20A              | **P3 - Séjour/Bureau/Four**      | 2.5 mm² | 15m      | 5 prises + four            |
| 7      | Disjoncteur               | 20A              | **Onduleur solaire AC-coupling** | 2.5 mm² | -        | **NOUVEAU CIRCUIT**        |
| 8-9    | Équipement DIN            | -                | **Monitoring onduleur**          | -       | -        | 2 modules DIN              |
| 10     | Disjoncteur               | 20A              | **sc_etage - Sous-tableau**      | 6 mm²   | 25m      | Alimentation étage         |
| 11-13  | -                         | -                | **LIBRE**                        | -       | -        | 3 emplacements disponibles |

**Charge maximale théorique** : 20A + 16A + 16A + 20A + 20A + 20A = 112A  
**Différentiel** : 40A adapté (diversité d'usage, onduleur en injection)

### Câblage

**Repérage des câbles** :
- **Chaudière** : Noir (étiquette "Chaudière+Routeur ECS")
- **L1** : Jaune (étiquette "Éclairage 1 - Salon/Garage")
- **L2** : Vert (étiquette "Éclairage 2 - Cuisine/Entrée")
- **P3** : Violet (étiquette "Séjour/Bureau/Four")
- **Onduleur** : Rouge/Noir rayé (étiquette "Onduleur Solaire")
- **sc_etage** : Gris (étiquette "Alimentation Étage")

---

## RANGÉE 3 - ECS et Extensions (30mA Type A)

### Schéma Détaillé

```
┌──────────────────────────────────────────────────────────────┐
│ Module │  1-2  │  3  │ 4 │ 5 │ 6 │ 7 │ 8 │ 9 │ 10 │ 11-13    │
├────────┼───────┼─────┼───┼───┼───┼───┼───┼───┼────┼──────────┤
│ Type   │ DIFF  │ DJ  │   │   │   │   │   │   │    │  LIBRE   │
│        │ 40A   │ 20A │   │   │   │   │   │   │    │          │
├────────┼───────┼─────┼───┼───┼───┼───┼───┼───┼────┼──────────┤
│Circuit │Type A │ ECS │   │   │   │   │   │   │    │          │
│        │ ▓▓▓▓  │Chauf│   │   │   │   │   │   │    │          │
│        │       │fe-ea│   │   │   │   │   │   │    │          │
└────────┴───────┴─────┴───┴───┴───┴───┴───┴───┴────┴──────────┘
         └──── Peigne d'alimentation horizontale ──────────────┘
```

### Détail des connexions

| Module | Équipement                | Type            | Circuit               | Section | Longueur | Notes                        |
| ------ | ------------------------- | --------------- | --------------------- | ------- | -------- | ---------------------------- |
| 1-2    | Interrupteur différentiel | 40A 30mA Type A | -                     | -       | -        | Obligatoire pour chauffe-eau |
| 3      | Disjoncteur               | 20A             | **ECS - Chauffe-eau** | 2.5 mm² | 5m       | Circuit dédié isolé          |
| 4-13   | -                         | -               | **LIBRE**             | -       | -        | 10 emplacements disponibles  |

**Charge maximale théorique** : 20A  
**Différentiel** : 40A (large marge pour extensions)

### Câblage

**Repérage des câbles** :
- **ECS** : Marron (étiquette "Chauffe-eau")

**Raison de l'isolation** :
- Permet mesure précise consommation hors ECS (Pince 2 sur Rangées 1+2)
- Facilite le routage solaire intelligent (surplus → ECS uniquement)

---

## Placement des Pinces Ampèremétriques

### Pince 1 : Mesure Globale (Routeur ECS)

```
┌─────────────────────┐
│  DISJONCTEUR EDF    │ ← Coupure générale
└──────────┬──────────┘
           │
      ╔════╪════╗
      ║  PINCE 1 ║ ← Mesure flux global (réseau/injection)
      ╚════╪════╝
           │
    ┌──────┴──────┐
    │ Différentiels│
    │ Rang 1+2+3  │
    └─────────────┘
```

**Fonction** : Mesure production/consommation globale
- Routeur ECS n'active ECS que si surplus sur cette mesure
- Évite que la batterie alimente l'ECS

### Pince 2 : Mesure Hors ECS (Onduleur)

```
┌─────────────────────┐
│ Alimentation        │
│ Rangées 1+2 UNIQUEMT│
└──────────┬──────────┘
           │
      ╔════╪════╗
      ║  PINCE 2 ║ ← Mesure consommation hors ECS
      ╚════╪════╝
           │
    ┌──────┴──────┐
    │   Rangées   │
    │    1 + 2    │
    └─────────────┘

    (Rangée 3 = ECS isolé)
```

**Fonction** : Mesure consommation maison (hors ECS)
- Onduleur décharge batterie si importation réseau détectée
- Optimise charge/décharge batterie selon consommation réelle

---

## Interconnexions et Câblage Interne

### Peignes d'Alimentation

**Peignes horizontaux** :
- 3× Peignes 13 modules (1 par rangée)
- Connexion Phase L depuis chaque différentiel
- Permet distribution sur tous les disjoncteurs de la rangée

**Peigne vertical** :
- Liaison entre les 3 interrupteurs différentiels
- Connexion depuis l'arrivée principale (après disjoncteur EDF)
- Phase L uniquement (neutre et terre sur borniers)

### Borniers

**Borniers de terre** :
- 3× Borniers 13 connexions (1 par rangée, en bas du tableau)
- Connexion à la barrette de terre principale
- Tous les circuits se raccordent ici

**Borniers de neutre** :
- 3× Borniers 13 connexions (1 par rangée, en haut)
- Connexion depuis la sortie de chaque différentiel
- Séparation obligatoire par rangée (après différentiel)

### Câblage Principal

```
ARRIVÉE EDF (haut du tableau)
    │
    ├─ Phase (rouge) → Peigne vertical → Différentiels
    ├─ Neutre (bleu) → Répartition par différentiel → Borniers neutre
    └─ Terre (vert/jaune) → Borniers de terre (barrette principale)
```

---

## Étiquetage et Repérage

### Méthode d'Étiquetage

**Solution retenue** : Scotch de peintre marqué au crayon bic
- Scotch de peintre blanc (masking tape) pour le repérage des fils et gaines
- Écriture au crayon bic (indélébile, résistant)
- Collé directement sur les **câbles/fils et gaines** à l'entrée du tableau et le long du parcours
- Permet identification rapide du circuit lors de la maintenance

**Avantages** :
- Économique et repositionnable
- Résistant aux manipulations répétées
- Visible le long du parcours des câbles
- Facile à mettre à jour en cas de modification

**Document de repérage** : [etiquettes_tableau.md](etiquettes_tableau.md)
- Fichier A4 imprimable avec toutes les étiquettes par rangée
- Format compact prêt à découper et coller
- Tableau synthétique récapitulatif pour la porte du tableau
- Peut servir de modèle pour le marquage au scotch de peintre

**Utilisation** :
- Imprimer et découper par rangée
- Ou utiliser comme référence pour marquer le scotch au crayon bic
- Plastifier le tableau synthétique et coller sur la porte avec le schéma unifilaire

### Étiquettes Recommandées

**Méthode d'étiquetage** : Scotch de peintre marqué au crayon bic
- Scotch de peintre blanc (masking tape)
- Écriture au crayon bic (indélébile, résistant)
- Collé sur le disjoncteur ou à côté

**Sur chaque disjoncteur** :
```
┌─────────────────────┐
│   P1                │ ← Identifiant circuit
│ PLAQUE CUISSON      │ ← Nom explicite
│   32A - 6mm²        │ ← Calibre et section
│   Cuisine           │ ← Localisation
└─────────────────────┘
```

**Format proposé pour tous les circuits** :

| ID        | Nom                     | Calibre | Section | Localisation           |
| --------- | ----------------------- | ------- | ------- | ---------------------- |
| P1        | Plaque cuisson          | 32A     | 6 mm²   | Cuisine                |
| P2        | Prises Buanderie/Garage | 20A     | 2.5 mm² | Buanderie + Garage     |
| P4        | Prises cuisine          | 20A     | 2.5 mm² | Cuisine (3 prises)     |
| Chaudière | Chaudière + Routeur     | 20A     | 2.5 mm² | Buanderie              |
| L1        | Éclairage 1             | 16A     | 1.5 mm² | Salon/Garage/Buanderie |
| L2        | Éclairage 2             | 16A     | 1.5 mm² | Cuisine/Entrée/WC      |
| P3        | Séjour/Bureau/Four      | 20A     | 2.5 mm² | Séjour/Bureau          |
| Onduleur  | Onduleur solaire        | 20A     | 2.5 mm² | Garage (équip.)        |
| sc_etage  | Alimentation étage      | 20A     | 6 mm²   | Sous-tableau étage     |
| ECS       | Chauffe-eau             | 20A     | 2.5 mm² | Buanderie              |

### Schéma Unifilaire

**À coller sur la porte du tableau** :
- Schéma complet de l'installation
- Référence : [schema_unifilaire_tableau.drawio](schema_unifilaire_tableau.drawio)
- Format plastifié A4 ou A3

---

## Installation Physique

### Dimensions du Tableau

**Coffret 3 rangées 13 modules** :
- Largeur : ~270 mm (13 modules × 18 mm + marges)
- Hauteur : ~540 mm (3 rangées × 150 mm + espace peignes)
- Profondeur : ~110 mm (avec porte)

### Positionnement Garage

**Hauteur recommandée** :
- Bas du tableau : **110-120 cm** du sol
- Centre disjoncteurs : **130-140 cm** (ergonomie optimale)
- Haut du tableau : **150-160 cm**

**Fixation** :
- 4 points de fixation (coins du coffret)
- Chevilles métal M8 ou M10 pour parpaing
- Niveau et aplomb vérifiés

### Entrées/Sorties de Câbles

**Entrées hautes** (depuis plafond) :
- Arrivée principale EDF (Phase/Neutre/Terre)
- Circuits depuis ancien tableau (via goulotte)

**Sorties basses** (optionnel) :
- Nouveau circuit onduleur solaire
- Extensions futures

**Passages latéraux** :
- Alimentation sous-tableau étage (vers plafond)

---

## Checklist d'Installation

### Avant Montage

- [ ] Tableau livré et vérifié (état, dimensions)
- [ ] Tous les disjoncteurs disponibles (récupérés + neufs)
- [ ] Différentiels neufs (2× Type A, 1× Type AC)
- [ ] Peignes horizontaux et vertical
- [ ] Borniers de terre et neutre (3 de chaque)
- [ ] Scotch de peintre et crayon bic (pour étiquetage)
- [ ] Câbles de rallonge préparés (avec repérage)
- [ ] Outils (tournevis, pince à dénuder, testeur)

### Montage du Tableau (J-1)

- [ ] Fixation du coffret au mur (niveau vérifié)
- [ ] Installation des 3 différentiels (modules 1-2 de chaque rangée)
- [ ] Installation du peigne vertical (liaison différentiels)
- [ ] Installation des peignes horizontaux (3 rangées)
- [ ] Installation des borniers de terre (bas)
- [ ] Installation des borniers de neutre (haut)
- [ ] Installation de tous les disjoncteurs récupérés
- [ ] Installation des nouveaux disjoncteurs (32A, 20A onduleur)
- [ ] Installation des obturateurs sur modules libres
- [ ] Câblage interne (peignes ↔ différentiels ↔ borniers)

### Raccordement des Circuits (Jour J)

- [ ] Coupure générale EDF
- [ ] Identification et étiquetage de tous les câbles anciens
- [ ] Raccordement circuit par circuit (test avant passage au suivant)
- [ ] Création circuit onduleur (nouveau câblage)
- [ ] Installation équipement mesure (2 modules DIN)
- [ ] Raccordement arrivée principale (Phase/Neutre/Terre)
- [ ] Installation des pinces ampèremétriques (Pince 1 et 2)
- [ ] Serrage de toutes les connexions (couple recommandé)
- [ ] Fermeture porte tableau

### Tests et Validation

- [ ] Test bouton TEST sur chaque différentiel → doit déclencher
- [ ] Réarmement différentiels
- [ ] Mise sous tension progressive (circuit par circuit)
- [ ] Test de fonctionnement de chaque circuit
- [ ] Mesure courants de fuite (comparaison avec ancien)
- [ ] Mesure résistance d'isolement (> 0,5 MΩ)
- [ ] Vérification des étiquettes et du schéma unifilaire
- [ ] Rangement de l'ancien tableau (conservation des pièces)

---

## Points de Vigilance

### ⚠️ Sécurité

1. **Coupure générale obligatoire** avant toute intervention
2. **Vérification absence de tension** (VAT) avant raccordement
3. **Port des EPI** (gants isolants, lunettes)
4. **Travail en binôme recommandé**

### ⚠️ Conformité

1. **Serrage des connexions** : couple recommandé par fabricant
2. **Sections de câbles respectées** : 1.5 / 2.5 / 6 mm²
3. **Couleurs normalisées** : Phase (rouge/noir), Neutre (bleu), Terre (vert/jaune)
4. **Séparation des neutres** : 1 bornier par différentiel (obligatoire)
5. **Test différentiels** : bouton TEST doit déclencher immédiatement

### ⚠️ Évolutions Futures

1. **Modules libres** : 18 emplacements disponibles
   - Rangée 1 : 8 modules (circuits prioritaires Type A)
   - Rangée 2 : 3 modules (circuits généraux Type AC)
   - Rangée 3 : 10 modules (circuits Type A ou extensions ECS)

2. **Extensions possibles** :
   - Borne de recharge VE (Type A, 32A dédié)
   - PAC future (Type A, circuit dédié)
   - Circuits extérieurs (éclairage jardin, piscine)
   - Domotique supplémentaire

---

## Documents Complémentaires

- [proposition_tableau_electrique.md](proposition_tableau_electrique.md) - Proposition technique complète
- [plan_implantation_tableau.md](plan_implantation_tableau.md) - Emplacement physique (garage)
- [schema_unifilaire_tableau.drawio](schema_unifilaire_tableau.drawio) - Schéma unifilaire
- [metré_rallonges_cables.md](metré_rallonges_cables.md) - Longueurs de câbles
- [checklist_validation.md](checklist_validation.md) - Tests post-installation

---

## Informations Manquantes (à compléter sur place)

### Avant Installation

- [ ] **Couleurs réelles des câbles existants** (peuvent différer du standard)
- [ ] **Numérotation des boîtes de dérivation** (pour traçabilité)
- [ ] **État physique des câbles** (vérification isolation lors du raccordement)
- [ ] **Mesure exacte des courants de fuite actuels** (comparaison avant/après)

### Pendant Installation

- [ ] **Photos avant/pendant/après** (documentation + Consuel)
- [ ] **Longueurs réelles des rallonges** (ajustement si nécessaire)
- [ ] **Emplacements précis des pinces ampèremétriques** (accessibilité vérifiée)
- [ ] **Positions exactes des boîtes de dérivation** (si ajout nécessaire)

### Après Installation

- [ ] **Mesures d'isolement par circuit** (valeurs en MΩ)
- [ ] **Courants de fuite mesurés** (comparaison avant/après)
- [ ] **Tests de déclenchement différentiels** (temps de réaction)
- [ ] **Consommations relevées** (validation pinces ampèremétriques)

---

**Auteur** : GitHub Copilot  
**Date** : 4 février 2026  
**Version** : 1.0  
**Statut** : ✅ Complet (infos manquantes = relevés sur place uniquement)
