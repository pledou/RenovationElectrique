# Repérage Tableau Électrique

**Date** : 26 mars 2026 | **Auteur** : Pierre LEDUC | **Version** : 1.0

---

## PAGE UNIQUE : BARRETTES 1 MODULE DIN

```bloc U+2500-U+257F
RANGÉE 1 - DIFF TYPE A 40A/30mA
(1 case = 1 module DIN)
┌──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┐
│ BAT  │ SOL  │ VMI  │  P1  │  P2  │  P3  │  P4  │ FOUR │      │      │      │
└──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┘

RANGÉE 2 - DIFF TYPE AC 40A/30mA
(1 case = 1 module DIN)
┌──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┐
│ CHD  │ SERV │  P5  │  P6  │  P7  │  L1  │  L2  │  L3  │  L4  │      │      │
└──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┘

RANGÉE 3 - DIFF TYPE A 40A/30mA (ECS ISOLÉ)
(1 case = 1 module DIN)
┌──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┐
│ ECS  │      │      │      │      │      │      │      │      │ MES1 │ MES2 │
└──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┘
```

<div style="page-break-before: always;"></div>

# Repérage Tableau Électrique

**Date** : 26 mars 2026 | **Auteur** : Pierre LEDUC | **Version** : 1.0

### LÉGENDE ABRÉGÉE

| Code        | Désignation                                              |
| :---------- | :------------------------------------------------------- |
| P1          | Prise dédiée 16A/4mm2 - Cuisine                          |
| P2          | Prises buanderie/garage 20A/2.5mm2                       |
| P3          | Prises séjour/bureau 20A/2.5mm2                          |
| P4          | Prises cuisine 20A/2.5mm2                                |
| FOUR        | Four ligne dédiée 20A/6mm2                               |
| BAT         | Onduleur batterie 20A/6mm2 (AC-coupling)                 |
| SOL         | Micro-onduleurs solaires jardin 20A/2.5mm2               |
| VMI         | Ventilation VMI 10A/1.5mm2 (éléments chauffants)         |
| CHD         | Chaudière 10A/2.5mm2                                     |
| L1          | Éclairage 1 10A/1.5mm2                                   |
| L2          | Éclairage 2 10A/1.5mm2                                   |
| L3          | Éclairage étage 10A/1.5mm2                               |
| L4          | Éclairage SdB, Ch4 10A/1.5mm2                            |
| SERV        | Services 2A/1.5mm2 - Routeur sol. + MES + pilotage chaud.|
| MES1/MES2   | Monitoring onduleur (2 modules) - Alimenté par SERV      |
| P5          | Prises étage 16A/2.5mm2                                  |
| P6          | Prises chambre 3 16A/2.5mm2                              |
| P7          | Prise palier 16A/2.5mm2                                  |
| ECS         | Chauffe-eau 20A/2.5mm2                                   |


---

## PINCES AMPÈREMÉTRIQUES

| **PINCE**   | **MESURE**            | **Positionnement**     |
| :---------- | :-------------------- | :--------------------- |
| **PINCE 1** | Mesure globale (EDF)  | Arrivée principale     |
| **PINCE 2** | Consommation hors ECS | Onduleur (rangées 1+2) |
| **PINCE 3** | Consommation R2       | Rangée 2               |

---

## MODE D'EMPLOI

1. **Imprimer** ce document sur papier **A4 portrait**.
2. Régler l'échelle d'impression à **129%** (car 18/14 = 1,286).
3. Désactiver les options du type **Ajuster à la page** / **Réduire les pages trop larges**.
4. Faire un test et mesurer la largeur intérieure d'une case : objectif **18 mm**.
5. **Aucune découpe nécessaire** — coller la feuille entière sur la porte du tableau ou face avant.
6. **Alternative pratique** : découper les 3 rangées individuellement (2-3 traits de ciseaux) pour un repérage par zone.
7. **Pour identification des câbles** : recopier au scotch de peintre en respectant les repères.

---

**Installation** : Garage, hauteur 110–150 cm  
**Format** : A4 portrait (210 × 297 mm)  
**Norme** : NF C 15-100  
**Mise à jour** : 26 mars 2026
