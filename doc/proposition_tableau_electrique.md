# Proposition de Tableau Électrique Conforme NF C 15-100

## Date de proposition
3 février 2026

## Principe général
Cette proposition vise à **minimiser les modifications sur les circuits existants** tout en assurant la conformité aux normes NF C 15-100 et en résolvant les problèmes de courants de fuite identifiés.

---

## Dimensionnement du Tableau

### Capacité requise
- **Nombre total de modules estimés : 21 modules** (répartis sur 3 rangées)
- Tableau proposé : **Coffret 3 rangées de 13 modules** (39 modules disponibles)
- **Emplacements libres : 18 modules** (disponibles pour extensions futures)
- **Sous-tableau étage conservé** (circuits VMI, P5, L3, L4, P6, P7 restent en place)

---

## Architecture du Tableau Proposé

### RANGÉE 1 - Circuits Rez-de-Chaussée Prioritaires (30mA Type A)

**Interrupteur différentiel 40A 30mA Type A** (obligatoire pour plaque de cuisson et lave-linge) - *2 modules*

| Module | Protection      | Circuit                          | Section | Longueur | Modification                    |
| ------ | --------------- | -------------------------------- | ------- | -------- | ------------------------------- |
| 3      | Disjoncteur 32A | **Plaque de cuisson** (P1)       | 6 mm²   | 5m       | **Changer disjoncteur 10A→32A** |
| 4      | Disjoncteur 20A | **Prises Buanderie/Garage** (P2) | 2.5 mm² | 12m      | Aucune                          |
| 5      | Disjoncteur 20A | **Prises cuisine** (P4)          | 2.5 mm² | 10m      | Aucune                          |
| 6-13   | -               | **Modules libres**               | -       | -        | Réserve (8 emplacements)        |

**Total Rangée 1 : 5 modules utilisés / 13 disponibles (8 libres)**

---

### RANGÉE 2 - Circuits Rez-de-Chaussée Généraux (30mA Type AC)

**Interrupteur différentiel 40A 30mA Type AC** - *2 modules*

| Module | Protection      | Circuit                                         | Section | Longueur | Modification                         |
| ------ | --------------- | ----------------------------------------------- | ------- | -------- | ------------------------------------ |
| 3      | Disjoncteur 20A | **Chaudière gaz + domotique + routeur ECS**     | 2.5 mm² | 12m      | Aucune                               |
| 4      | Disjoncteur 16A | **Éclairage 1** (L1)                            | 1.5 mm² | 15m      | Aucune                               |
| 5      | Disjoncteur 16A | **Éclairage 2** (L2)                            | 1.5 mm² | 10m      | Aucune                               |
| 6      | Disjoncteur 20A | **Prises Séjour/Bureau/Four** (P3)              | 2.5 mm² | 15m      | Aucune                               |
| 7      | Disjoncteur 20A | **Onduleur solaire batterie (AC-coupling)**     | 2.5 mm² | -        | **NOUVEAU CIRCUIT**                  |
| 8      | -               | **Équipement mesure onduleur (2 modules)**      | -       | -        | **NOUVEAU - Monitoring AC-coupling** |
| 9      | -               | *(suite équipement mesure)*                     | -       | -        | -                                    |
| 10     | Disjoncteur 20A | **Alimentation sous-compteur étage** (sc_etage) | 6 mm²   | 25m      | Aucune                               |
| 11-13  | -               | **Modules libres**                              | -       | -        | Réserve (3 emplacements)             |

**Total Rangée 2 : 10 modules utilisés / 13 disponibles (3 libres)**

> **Note routeur solaire ECS** : Le routeur solaire est commandé par le circuit de la chaudière (Module 3) et pilote la puissance sur le circuit ECS existant (Rangée 3, Module 3). Aucun circuit dédié supplémentaire n'est nécessaire.

---

### RANGÉE 3 - ECS et Extensions Futures (30mA Type A)

**Interrupteur différentiel 40A 30mA Type A** - *2 modules*

| Module | Protection      | Circuit                     | Section | Longueur | Modification |
| ------ | --------------- | --------------------------- | ------- | -------- | ------------ |
| 3      | Disjoncteur 20A | **Chauffe-eau** (sanitaire) | 2.5 mm² | 5m       | Aucune       |
| 4-13   | -               | **Modules libres**          | -       | -        | Réserve (7 emplacements) |

**Total Rangée 3 : 3 modules utilisés / 13 disponibles (7 libres)**

> **Note isolation ECS** : L'ECS est isolé sur une rangée dédiée pour permettre une mesure précise de la consommation hors ECS via la Pince 2 (placée sur les Rangées 1+2).

---

### Placement des Pinces Ampèremétriques

#### Pince 1 : Mesure Production/Consommation Globale
- **Localisation** : Sur le **câble d'arrivée principal APRÈS le disjoncteur EDF et AVANT tous les différentiels**
- **Fonction** : Mesure du flux d'énergie global (consommation totale réseau / injection réseau)
- **Équipement associé** : Routeur solaire ECS (commandé depuis circuit chaudière)
- **Objectif** : Permet au routeur solaire de ne router vers l'ECS que le surplus réel (hors consommation maison)

#### Pince 2 : Mesure Consommation Hors ECS
- **Localisation** : Sur les **câbles d'alimentation des Rangées 1+2** (après différentiels) ou en amont des différentiels Rangées 1+2
- **Fonction** : Mesure de toute la consommation de la maison SAUF l'ECS
- **Équipement associé** : Dispositif de monitoring de l'onduleur (2 modules DIN Rangée 2)
- **Objectif** : Permet à l'onduleur de réguler la charge/décharge de la batterie en fonction de la consommation totale

#### Logique de Gestion des Flux
```
Production Solaire
    ↓
Consommation Instantanée Maison (priorité 1) ← Mesurée par Pince 1 (hors ECS)
    ↓
Surplus → Charge Batterie (priorité 2) ← Contrôle Pince 2 (flux global)
    ↓
Surplus Batterie Pleine → ECS (priorité 3) ← Routage si surplus Pince 1
```

**Principe** :
- **Pince 1** (arrivée principale) mesure le flux global : le routeur solaire ne route vers l'ECS que si surplus sur cette mesure (évite que la batterie alimente l'ECS)
- **Pince 2** (Rangées 1+2) mesure la consommation hors ECS : si importation réseau détectée, l'onduleur décharge la batterie
- **Architecture tableau** : L'ECS isolé sur Rangée 3 permet à la Pince 2 de mesurer uniquement les Rangées 1+2 (toute la maison sauf ECS)

---

### SOUS-TABLEAU ÉTAGE - Mise à niveau requise

**Alimentation** : Câble 6mm² depuis le tableau principal (disjoncteur 20A - Rangée 2 Module 10)

**⚠️ MODIFICATIONS IMPORTANTES** : 
1. Ajout d'un interrupteur différentiel 30mA obligatoire
2. **Déplacement du tableau à hauteur réglementaire** (actuellement au plafond à 250cm)
3. **⚠️ REMPLACEMENT DU TABLEAU OBLIGATOIRE**

**Analyse capacité actuelle** :
- **Tableau actuel : < 13 modules** (capacité insuffisante confirmée)
- Différentiel 30mA à ajouter : **2 modules**
- Circuits existants : 6 disjoncteurs = **6 modules**
- **Total nécessaire : 8 modules minimum**
- **→ Remplacement obligatoire par coffret 13 modules** (laissera 5 modules libres après installation)
- **Hauteur d'installation : 1,70-1,80m** (limite haute réglementaire pour sécurité enfants)

**Protection différentielle à ajouter** :
- **Interrupteur différentiel 40A 30mA Type AC** - *2 modules*

**Circuits maintenus sur le sous-tableau étage** :
- ✅ **VMI** (ventilation) - Disjoncteur 16A - 1.5 mm² - 18m
- ✅ **P5** (Prises étage) - Disjoncteur 16A - 2.5 mm² - 30m
- ✅ **L3** (Éclairage étage) - Disjoncteur 16A - 1.5 mm² - 25m
- ✅ **L4** (Éclairage salle de bains) - Disjoncteur 16A - 1.5 mm² - 15m
- ✅ **P6** (Prises chambre 3) - Disjoncteur 10A - 2.5 mm² - 10m
- ✅ **P7** (Prise palier) - Disjoncteur 10A - 2.5 mm² - 10m

**Travaux à réaliser sur le sous-tableau** :
1. **✅ Capacité vérifiée : < 13 modules → Remplacement obligatoire**
2. **Remplacement par coffret 13 modules** avec porte (2 modules différentiel + 6 disjoncteurs + 5 modules libres)
3. **Installation différentiel 30mA Type AC** (obligatoire selon NF C 15-100)
4. **Installation peigne de distribution et borniers** (remplacement des dés à visser)
5. **Installation du tableau en hauteur** (de 250cm au plafond → **1,70-1,80m du sol** pour limiter accès enfants)
6. **Rallonge des câbles si nécessaire** (ajout 0,70-1,00m par circuit selon nouvelle position)
7. **Raccordement de tous les circuits en aval du différentiel**

> **📋 Justification norme** : La NF C 15-100 impose qu'un tableau divisionnaire (sous-tableau) soit équipé de son propre dispositif différentiel 30mA pour assurer la protection des personnes. L'alimentation depuis le tableau principal par un disjoncteur 20A assure la protection contre les surintensités, mais ne remplace pas le différentiel local.

> **📏 Hauteur réglementaire** : La NF C 15-100 impose que l'appareillage soit installé entre **0,90m et 1,80m du sol**. Un tableau au plafond (250cm) est non-conforme. **Hauteur retenue : 1,70-1,80m** (limite haute réglementaire) pour limiter l'accès par les enfants tout en permettant l'intervention des adultes.

> **🔧 Avantages de cette mise à niveau** :
> - **Conformité normative** : Respect intégral NF C 15-100 (différentiel + hauteur réglementaire)
> - **Sélectivité améliorée** : En cas de défaut à l'étage, seul le différentiel étage déclenche (pas celui du RdC)
> - **Sécurité renforcée** : Protection différentielle locale + isolation des courants de fuite étage/RdC
> - **Sécurité enfants** : Tableau en hauteur (1,70-1,80m) limitant l'accès par les enfants, conforme NF C 15-100 (0,90-1,80m)
> - **Fiabilité** : Peigne de distribution plus fiable que les dés à visser (moins de risque de faux contact)

---

## Modifications Requises sur les Circuits Existants

### ✅ Modifications MINIMALES

1. **Circuit P1 (Plaque de cuisson) - MODIFICATION MINEURE**
   - **État constaté** : Circuit déjà câblé en 6mm² sur 5m avec disjoncteur 10A ✅
   - **Action** : Remplacer uniquement le disjoncteur 10A par un 32A
   - **Justification** : Le câblage 6mm² est déjà conforme, seule la protection est sous-dimensionnée
   - **Impact** : Minimal - simple remplacement de disjoncteur (pas de tirage de câble)

2. **Nouveau circuit onduleur solaire AC-coupling - CRÉATION NOUVELLE**
   - **Action** : Créer un circuit dédié pour l'onduleur avec batterie en AC-coupling
   - **Protection** : Disjoncteur 20A sur différentiel Type AC
   - **Équipement de mesure** : 2 modules DIN pour le monitoring (Rangée 2)
   - **Justification** : Gestion de la production solaire et stockage batterie

3. **Routeur solaire ECS - INTÉGRÉ AUX CIRCUITS EXISTANTS**
   - **Commande** : Sur circuit chaudière existant (Rangée 2, Module 3)
   - **Puissance** : Pilote le circuit ECS existant (Rangée 3, Module 3)
   - **Pince ampèremétrique (Pince 2)** : Mesure consommation hors ECS (Rangées 1+2)
   - **Justification** : Routage du surplus solaire vers l'ECS après charge batterie, sans circuit supplémentaire

4. **Sous-tableau étage - MISE À NIVEAU OBLIGATOIRE**
   - **Préalable** : ✅ Capacité vérifiée : < 13 modules → Remplacement obligatoire
   - **Action 1** : Remplacement du tableau par coffret 13 modules (capacité insuffisante confirmée)
   - **Action 2** : Installation d'un interrupteur différentiel 40A 30mA Type AC (2 modules)
   - **Action 3** : Déplacement du tableau du plafond (250cm) vers installation en hauteur (1,70-1,80m du sol pour sécurité enfants)
   - **Action 4** : Installation peigne de distribution et borniers (remplacement des dés à visser)
   - **Rallonge câbles** : Selon nouvelle position (ajout de 0,70-1,00m par circuit si nécessaire)
   - **Justification** : Conformité NF C 15-100 (différentiel obligatoire + hauteur 0,90-1,80m + capacité suffisante) + amélioration sélectivité, sécurité enfants et isolation des courants de fuite étage/RdC

---

## Justifications Techniques

### Choix des Différentiels

**Type A (Rangées 1 et 3)** - Obligatoire pour :
- Plaque de cuisson (électronique de puissance)
- Lave-linge (variateurs électroniques)
- Chauffe-eau (équipé de triac ou routeur solaire)

**Type AC (Rangée 2 et sous-tableau étage)** - Suffisant pour :
- Éclairages
- Prises standards
- Circuits bureautiques et domotique
- Ventilation (VMI)

### Répartition des Circuits

**Équilibrage de charge** :
- Rangée 1 : ~32A + 20A + 20A = **72A max théorique** (différentiel 40A adapté)
- Rangée 2 : ~20A + 16A + 16A + 20A + 20A + 20A = **112A max théorique** (différentiel 40A adapté avec diversité)
- Rangée 3 : ~20A = **20A max théorique** (différentiel 40A, large marge)
- Sous-tableau étage : ~16A + 16A + 16A + 16A + 10A + 10A = **84A max théorique** (alimenté par disjoncteur 20A)

> **Note** : En pratique, tous les circuits ne sont jamais à leur maximum simultanément. La diversité d'usage justifie les différentiels 40A. L'onduleur solaire fonctionne en injection/régulation (consommation nette faible), et le routeur ECS est intégré aux circuits existants (chaudière + ECS Rangée 3). L'isolation de l'ECS sur la Rangée 3 facilite la mesure de consommation hors ECS pour optimiser le routage solaire. Le sous-tableau étage est protégé par un disjoncteur 20A en tête ET équipé d'un différentiel 30mA local, assurant une double protection et une sélectivité optimale.

### Sélectivité

- **Différentiel EDF 500mA** en tête (maintenu)
- **Différentiels 30mA tableau principal** en aval (3 différentiels : 2x Type A + 1x Type AC)
- **Différentiel 30mA sous-tableau étage** en aval du disjoncteur 20A
- **Sélectivité verticale assurée** : 500mA / 30mA = facteur 16,7 (recommandation : >3)
- **Sélectivité horizontale** : Chaque différentiel protège une zone distincte (Rangées 1, 2, 3 et sous-tableau)

> **Note production solaire** : L'onduleur AC-coupling injecte l'énergie en aval des différentiels 30mA, garantissant la protection différentielle même lors de la production. Les pinces ampèremétriques permettent la régulation intelligente des flux sans compromettre la sélectivité.

> **Note sous-tableau** : Le différentiel 30mA du sous-tableau étage assure une sélectivité totale : en cas de défaut à l'étage, seul ce différentiel déclenche, préservant l'alimentation du RdC. Inversement, un défaut au RdC ne coupe pas l'étage.

---

## Points de Conformité NF C 15-100

### ✅ Circuits respectés

| Exigence                            | Conformité | Commentaire                                                      |
| ----------------------------------- | ---------- | ---------------------------------------------------------------- |
| **Plaque de cuisson circuit dédié** | ✅          | Circuit P1 dédié 32A Type A                                      |
| **Four circuit dédié ou mutualisé** | ✅          | Sur P3 (20A) - accepté jusqu'à 3680W                             |
| **Lave-linge sur Type A**           | ✅          | P2 sur différentiel Type A                                       |
| **Chauffe-eau circuit dédié**       | ✅          | 20A dédié                                                        |
| **Prises 16A max 5 par circuit**    | ✅          | P2:5, P3:5, P4:3, P5:3, P6:2, P7:1 - tous conformes              |
| **Prises cuisine minimum 6**        | ⚠️          | **P4 a 3 prises (+ P1 plaque dédiée) - À vérifier si suffisant** |
| **Éclairages 16A max 8 points**     | ✅          | L1:8 points, L2:3, L3:5, L4:2 - tous conformes                   |
| **Sections conformes**              | ✅          | 1.5mm² éclairages, 2.5mm² prises, 6mm² plaque                    |
| **Protection différentielle 30mA**  | ✅          | 3 différentiels 30mA tableau principal + 1 différentiel sous-tableau étage |

---

## Circuits Conservés Sans Modification

**13 circuits sur 15 sont conservés tel quel** :

### Sur le tableau principal :
- ✅ Chaudière
- ✅ L1, L2 (éclairages RdC)
- ✅ P1 (Plaque de cuisson - câblage 6mm² OK, changement disjoncteur uniquement)
- ✅ P2 (Buanderie/Garage)
- ✅ P3 (Séjour/Bureau/Four)
- ✅ P4 (Cuisine)
- ✅ sc_etage (alimentation sous-tableau)
- ✅ sanitaire (Chauffe-eau)

### Sur le sous-tableau étage (câblage conservé, différentiel ajouté) :
- ✅ VMI (ventilation) - **Câblage inchangé**
- ✅ P5 (Prises étage) - **Câblage inchangé**
- ✅ L3, L4 (Éclairages étage) - **Câblage inchangé**
- ✅ P6, P7 (Prises chambres) - **Câblage inchangé**
- ⚠️ **Ajout différentiel 30mA** (obligatoire NF C 15-100)
- ⚠️ **Remplacement dés à visser par peigne** (amélioration fiabilité)

---

## Résolution des Problèmes Identifiés

### Courants de fuite sur le neutre
**Solution adoptée** :
- Répartition sur **4 différentiels 30mA distincts** (3 au tableau principal + 1 au sous-tableau étage)
- En cas de défaut, seule une partie de l'installation est coupée
- Facilite le diagnostic (isolation par rangée au RdC, isolation totale étage)
- **Sélectivité géographique** : Un défaut à l'étage ne coupe pas le RdC et inversement

### Câbles hors conduit
**À traiter séparément** :
- Défauts B8.3.e identifiés sur P3, P4 et volets roulants
- **Recommandation** : Mise en conduit ou goulotte lors de la rénovation (non traité dans cette proposition de tableau)

### Prises sans terre
**À traiter séparément** :
- Défauts B3.3.6 sur P4 et P5 (chambres)
- **Recommandation** : Remplacement des prises et vérification de la continuité de terre (non traité dans cette proposition de tableau)

---

## Liste du Matériel Proposé

### Tableau et protections

| Quantité | Désignation                                          | Référence exemple                              |
| -------- | ---------------------------------------------------- | ---------------------------------------------- |
| 1        | Coffret 3 rangées 13 modules avec porte              | Schneider Rési9 ou équivalent                  |
| 2        | Interrupteur différentiel 40A 30mA Type A bipolaire  | Schneider Rési9 XE ou équivalent               |
| 1        | Interrupteur différentiel 40A 30mA Type AC bipolaire | Schneider Rési9 XE ou équivalent               |
| 1        | Disjoncteur 32A courbe C                             | Pour plaque cuisson                            |
| 1        | Disjoncteur 20A courbe C                             | Pour onduleur solaire (**nouveau circuit**)    |
| 1        | Disjoncteur 20A courbe C                             | Pour microonduleurs jardin (**nouveau circuit**) |
| 1        | Parafoudre Type 2 (optionnel mais recommandé)        | Pour protection générale et production solaire |
| 3        | Bornier de terre                                     | 13 connexions minimum par rangée               |
| 3        | Bornier de neutre par rangée                         | 13 connexions par rangée                       |
| 3        | Peigne d'alimentation horizontal                     | 13 modules par rangée                          |
| 1        | Peigne d'alimentation vertical                       | Liaison entre différentiels                    |

### Matériel sous-tableau étage

**Remplacement obligatoire (tableau actuel < 13 modules)** :

| Quantité | Désignation                                          | Référence exemple            |
| -------- | ---------------------------------------------------- | ---------------------------- |
| 1        | **Coffret 13 modules avec porte** | **Schneider Rési9 ou équivalent** |
| 1        | Interrupteur différentiel 40A 30mA Type AC bipolaire | Schneider Rési9 XE ou équivalent |
| 1        | Peigne d'alimentation horizontal | 13 modules |
| 1        | Bornier de neutre | 13 connexions |
| 1        | Bornier de terre | 13 connexions |
| Variable | Rallonges de câbles | Selon circuits (0,70-1,00m par circuit si nécessaire) |
| 1        | Support de fixation murale | Pour installation en hauteur (1,70-1,80m) |

### Disjoncteurs existants réutilisés

✅ **Vous possédez déjà ces disjoncteurs qui seront démontés de l'ancien tableau et réinstallés dans le nouveau** :

| Quantité disponible | Quantité nécessaire | Type                     | Utilisation dans le nouveau tableau      |
| ------------------- | ------------------- | ------------------------ | ---------------------------------------- |
| 5                   | 5                   | Disjoncteur 20A courbe C | Chauffe-eau, P2, P4, Chaudière, sc_etage |
| 4                   | 2                   | Disjoncteur 16A courbe C | L1, L2                                   |

> **📝 Note importante** : Vous avez 4 disjoncteurs C16 mais seulement 2 sont nécessaires sur le tableau principal. Les 2 autres restent en réserve ou peuvent rester sur le sous-tableau étage. Pour le **nouveau circuit onduleur solaire**, vous devrez acheter **1 disjoncteur C20 supplémentaire**. Le routeur ECS utilise les circuits existants (chaudière + ECS), aucun disjoncteur supplémentaire n'est nécessaire.

### Accessoires

| Quantité | Désignation                                    |
| -------- | ---------------------------------------------- |
| 1 lot    | Étiquettes de repérage pour circuits           |
| 1 lot    | Obturateurs pour modules vides                 |
| 1        | Schéma unifilaire plastifié à coller sur porte |

---

## Procédure de Remplacement Recommandée

### Phase 1 : Préparation (J-1)
1. Installation du nouveau tableau à côté de l'ancien
2. Câblage du nouveau tableau (peignes, différentiels)
3. **Démontage et récupération des disjoncteurs C20 et C16 de l'ancien tableau**
4. Installation des disjoncteurs récupérés dans le nouveau tableau
5. Préparation des câbles de raccordement

### Phase 2 : Bascule Progressive (Jour J)
1. **Coupure minimale** : Basculer circuit par circuit
2. Circuits prioritaires en dernier (chaudière, réfrigérateur)
3. Test de chaque circuit avant passage au suivant
4. **Durée estimée** : 3-4 heures (pas de nouveau câblage)

### Phase 3 : Validation
1. Test des différentiels (bouton TEST)
2. Mesure de l'isolement par circuit
3. Vérification des courants de fuite
4. Documentation et remise du schéma unifilaire

### Phase 4 : Remplacement sous-tableau étage (peut être fait avant ou après)

**Tableau actuel < 13 modules → Remplacement obligatoire** :
1. **Dépose du tableau existant** du plafond (récupération des disjoncteurs)
2. **Installation support de fixation** en hauteur (1,70-1,80m du sol pour limiter accès enfants)
3. **Installation nouveau coffret 13 modules** à la bonne hauteur
4. **Rallonge des câbles** si nécessaire (ajout 0,70-1,00m par circuit)
5. **Installation différentiel 30mA + peigne + borniers** dans le nouveau coffret
6. **Remontage des disjoncteurs récupérés** (6 disjoncteurs pour VMI, P5, L3, L4, P6, P7)
7. **Raccordement de tous les circuits** en aval du différentiel
8. **Test fonctionnel** : vérification protection différentielle et sélectivité
9. **Durée estimée** : **9-14 heures** (étage uniquement)

---

## Points d'Attention Particuliers

### 🔴 Circuits avec défauts identifiés à corriger ultérieurement

1. **L1 (Éclairage 1)** : Problèmes de phase/neutre croisés avec L2 et L3
   - Palier étage : "neutre ou phase sur L3"
   - Garage, Buanderie, Palier RdC : "neutre ou phase sur L2"
   - **Action recommandée** : Traçage et correction du câblage

2. **P3 et P4** : Câbles hors conduit et prises non conformes
   - **Action recommandée** : Mise en conduit et remplacement des prises

3. **P5 (Étage)** : Prises 2 pôles sans terre
   - **Action recommandée** : Remplacement des prises et vérification terre

### 🟡 Vérifications à effectuer avant installation

- ~~Compter le nombre exact de points d'éclairage par circuit (max 8)~~ **✅ Vérifié : L1=8, L2=3, L3=5, L4=2**
- ~~Compter le nombre exact de prises par circuit (max 8 si 16A, 12 si 20A)~~ **✅ Vérifié : tous conformes**
- **⚠️ Vérifier si P4 (3 prises) + équipements non répertoriés suffisent pour la cuisine** (norme : 6 prises mini)
- Vérifier l'état des conducteurs existants (isolement)
- Mesurer les courants de fuite actuels pour comparaison

---

## Coût Estimatif

### Matériel

**Tableau principal** :
- Tableau 3 rangées et protections : **380-520 €**
- 1 différentiel Type A supplémentaire : **40-60 €**
- Disjoncteur 32A supplémentaire : **15-25 €**
- 2 disjoncteurs 20A (onduleur + microonduleurs) : **30-50 €**
- Accessoires et petits matériels : **70-100 €**
- **Sous-total tableau principal : 535-755 €**

**Sous-tableau étage** :

*Remplacement obligatoire (tableau actuel < 13 modules)* :
- **Coffret 13 modules avec porte : 50-80 €**
- 1 différentiel 40A 30mA Type AC : **40-60 €**
- Peigne de distribution : **15-25 €**
- Borniers (neutre + terre) : **10-20 €**
- Rallonges câbles (si nécessaire) : **20-40 €**
- Support fixation : **10-15 €**
- **Sous-total sous-tableau : 145-240 €**

**Total matériel : 665-970 €**

> **💰 Économie réalisée** : La réutilisation de vos 5 disjoncteurs C20 et 2 disjoncteurs C16 existants vous fait économiser environ **70-100 €**. Le routeur ECS utilisant les circuits existants (chaudière + ECS), aucun circuit supplémentaire n'est nécessaire, économisant **~150-200 € supplémentaires**.

> **📝 Note** : L'équipement de mesure AC-coupling (2 modules DIN) et les pinces ampèremétriques ne sont pas inclus dans ce budget car fournis avec votre système solaire.

---

## Temps de Chantier Estimés (Réalisation en Autoconstruction)

### Tableau principal

**Phase 1 : Préparation** :
- Installation coffret et câblage interne (peignes, différentiels) : **3-4 heures**
- Démontage et récupération disjoncteurs ancien tableau : **1 heure**
- Préparation câbles de raccordement : **1-2 heures**
- **Total Phase 1 : 5-7 heures**

**Phase 2 : Bascule et raccordement** :
- Bascule progressive circuit par circuit : **3-4 heures**
- Création circuit onduleur solaire : **1-2 heures**
- Installation équipement mesure AC-coupling : **1 heure**
- **Total Phase 2 : 5-7 heures**

**Phase 3 : Tests et validation** :
- Tests différentiels et isolement : **1-2 heures**
- Documentation et étiquetage : **1 heure**
- **Total Phase 3 : 2-3 heures**

**Total tableau principal : 12-17 heures** (sur 2-3 jours avec pauses)

### Sous-tableau étage

**Remplacement obligatoire (tableau actuel < 13 modules)** :
- Dépose ancien tableau : **1 heure**
- Installation nouveau coffret en hauteur : **1-2 heures**
- Rallonge câbles si nécessaire : **1-2 heures** (descente moindre depuis plafond)
- Installation différentiel, peigne et borniers : **2-3 heures**
- Raccordement tous circuits : **2-3 heures**
- Tests et validation : **1-2 heures**
- **Total sous-tableau : 8-13 heures**

### **TEMPS TOTAL PROJET**
- Tableau principal : **12-17 heures**
- Sous-tableau étage : **8-13 heures**
- **TOTAL : 20-30 heures**

> **⏱️ Planning recommandé** : 
> - Tableau principal : **2 jours** (week-end)
> - Sous-tableau étage : **1 jour** (week-end suivant)
> - Marge de sécurité : **+20-30%** pour imprévus

> **💡 Conseil** : Prévoir un électricien pour validation finale et Consuel (obligatoire pour conformité)

---

## Coût Total du Projet (Autoconstruction)

### Budget matériel uniquement

**Remplacement sous-tableau confirmé (< 13 modules)** :
- Matériel tableau principal : **535-755 €**
- Matériel sous-tableau (avec nouveau coffret 13 modules) : **145-240 €**
- **TOTAL MATÉRIEL : 680-995 €**

### Budget avec validation professionnelle (recommandé)
- Visite électricien pour validation finale : **150-250 €**
- Consuel (certification obligatoire) : **150-200 €**
- **Supplément validation : 300-450 €**

### **BUDGET TOTAL ESTIMÉ**
- **Sans validation** : **680-995 €** (matériel uniquement)
- **Avec validation professionnelle** : **980-1445 €** (matériel + validation + Consuel)

> **Note** : Ces prix sont indicatifs (février 2026) et peuvent varier selon les régions, prestataires et marques d'équipements de monitoring solaire choisis.

---

## Avantages de cette Proposition

✅ **Conformité** : Respect intégral de la NF C 15-100 (incluant différentiel obligatoire sur sous-tableau)  
✅ **Minimise les travaux** : 13 circuits sur 15 conservés sans modification de câblage  
✅ **Sous-tableau mis à niveau** : Ajout différentiel 30mA + peigne de distribution (conformité + fiabilité)  
✅ **Sécurité** : 4 différentiels 30mA au total (3 tableau principal + 1 sous-tableau) pour isolation optimale  
✅ **Production solaire intégrée** : Gestion intelligente batterie + routeur ECS avec contrôle des flux optimisé  
✅ **Évolutivité** : **17 emplacements libres** pour extensions futures (8 en Rangée 1, 2 en Rangée 2, 7 en Rangée 3)  
✅ **Diagnostic facilité** : Séparation claire circuits prioritaires/généraux/ECS + isolation totale étage/RdC  
✅ **Optimisation énergétique** : ECS isolé permettant mesure précise consommation hors ECS, priorité consommation > batterie > ECS  
✅ **Sélectivité maximale** : Défaut étage ne coupe pas RdC et inversement  

---

## Conclusion

Cette proposition permet de **mettre en conformité votre installation avec un minimum de modifications** tout en intégrant votre système de production solaire :
- **2 circuits à créer** (onduleur solaire AC-coupling + microonduleurs jardin)
- **1 circuit à modifier** (P1 - changement disjoncteur 10A→32A uniquement)
- **13 circuits conservés à l'identique** (câblage inchangé)
- **Sous-tableau étage : mise à niveau obligatoire** (ajout différentiel 30mA + peigne de distribution + **déplacement à hauteur réglementaire**)
- **Routeur solaire ECS** : intégré aux circuits existants (commande sur chaudière, puissance sur ECS)
- **2 pinces ampèremétriques** pour gestion intelligente des flux énergétiques
- **2 modules DIN** pour équipement de mesure AC-coupling

### Logique de Priorité Énergétique Implémentée
1. **Consommation instantanée** (priorité absolue)
2. **Charge batterie** si surplus (Pince 1 contrôle flux réseau)
3. **Routage vers ECS** si batterie pleine (Pince 2 sur circuit ECS empêche décharge batterie vers ECS)

### Intégration Routeur Solaire ECS
- **Commande/Pilotage** : Circuit chaudière existant (Rangée 2, Module 3)
- **Puissance** : Circuit ECS existant (Rangée 3, Module 3)
- **Pince 2 (mesure hors ECS)** : Placée sur Rangées 1+2 pour mesurer toute la consommation sauf ECS et piloter le routeur ECS
- **Pince 1 (mesure globale)** : Placée sur arrivée principale pour le pilotage de l'onduleur/batterie
- **Architecture optimisée** : ECS isolé sur Rangée 3 dédiée, permettant une mesure précise de la consommation hors ECS
- **Avantage** : Microonduleurs sur circuit dédié sécurisé + 17 emplacements libres pour extensions futures

Les défauts identifiés sur les câblages et prises pourront être traités ultérieurement, circuit par circuit, sans nécessiter une nouvelle intervention sur le tableau.

---

## Document Complémentaire à Produire

- [x] Schéma unifilaire détaillé (réalisé : [schema_unifilaire_tableau.drawio](schema_unifilaire_tableau.drawio))
- [x] Plan d'implantation du nouveau tableau (réalisé : [plan_implantation_tableau.md](plan_implantation_tableau.md) + [plan_organisation_tableau.md](plan_organisation_tableau.md))
- [ ] Fiche de repérage des circuits existants (couleurs, boîtes de dérivation)
- [ ] Checklist de validation (voir `doc/checklist_validation.md`)

---

**Auteur** : GitHub Copilot  
**Date** : 3 février 2026  
**Version** : 1.0
