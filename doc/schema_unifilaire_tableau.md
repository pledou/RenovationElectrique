# Schéma unifilaire tableau principal (NF C 15-100)

Date : 17 février 2026  
Source : [plan_organisation_tableau.md](plan_organisation_tableau.md)

## Schéma (texte unifilaire)

```text
Réseau ENEDIS
   │
   └── Disjoncteur de branchement 500 mA
         │
         ├── [Pince 1] Mesure flux global (après DB, avant répartition)
         │
         ├── Rangée 1 : ID 40A / 30mA Type A
         │     ├── DJ 32A  : P1 Plaque de cuisson (6 mm²)
         │     ├── DJ 20A  : P2 Prises buanderie/garage (2,5 mm²)
         │     ├── DJ 20A  : P3 Prises séjour/bureau/four (2,5 mm²)
         │     ├── DJ 20A  : P4 Prises cuisine (2,5 mm²)
         │     ├── DJ 20A  : Onduleur solaire AC-coupling (2,5 mm²)
         │     ├── DJ 20A  : Microonduleurs jardin (2,5 mm²)
         │     ├── DJ 2A   : VMI étage (1,5 mm²)
         │     └── Réserve : 4 modules
         │
         ├── Rangée 2 : ID 40A / 30mA Type AC
         │     ├── DJ 20A  : Chaudière + domotique + routeur ECS (2,5 mm²)
         │     ├── DJ 16A  : L1 Éclairage 1 (1,5 mm²)
         │     ├── DJ 16A  : L2 Éclairage 2 (1,5 mm²)
         │     ├── DJ 16A  : L3 Éclairage étage (1,5 mm²)
         │     ├── DJ 16A  : L4 Éclairage salle de bains (1,5 mm²)
         │     ├── 2 modules DIN : Équipement mesure onduleur
         │     ├── DJ 16A  : P5 Prises étage (2,5 mm²)
         │     ├── DJ 10A  : P6 Prises chambre 3 (2,5 mm²)
         │     ├── DJ 10A  : P7 Prise palier (2,5 mm²)
         │     └── Réserve : 1 module
         │
         └── Rangée 3 : ID 40A / 30mA Type A
               ├── DJ 20A  : ECS Chauffe-eau (2,5 mm²)
               └── Réserve : 10 modules

[Pince 2] Mesure consommation hors ECS sur l'alimentation des rangées 1+2.
```

## Rappels de conformité NF C 15-100 (appliqués ici)

- Protection différentielle 30 mA sur l'ensemble des circuits terminaux.
- Type A affecté aux circuits avec électronique de puissance (plaque, ECS via routeur, etc.).
- Sections et calibres cohérents :
  - 6 mm² / 32A pour plaque.
  - 2,5 mm² / 20A (prises et circuits dédiés concernés).
  - 1,5 mm² / 16A (éclairage).
  - 1,5 mm² / 2A (VMI/commande faible puissance).
- Sous-tableau étage supprimé : intégration directe des circuits VMI, P5, L3, L4, P6, P7 au tableau principal.

## Références

- [plan_organisation_tableau.md](plan_organisation_tableau.md)
- [proposition_tableau_electrique.md](proposition_tableau_electrique.md)
- [etiquettes_tableau.md](etiquettes_tableau.md)
