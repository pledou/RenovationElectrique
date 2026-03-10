# Renovation Electrique

## État d'avancement du projet

**Dernière mise à jour** : 9 mars 2026

| Phase | État | Détails |
|-------|------|---------|
| 📋 Inventaire installation | ✅ Complété | `data/installation.yaml` - 14 circuits identifiés |
| 📐 Plans et schémas | ✅ Complétés | Plans RdC/Étage + schéma unifilaire |
| 🔍 Analyse défauts | ✅ Complétée | Fuites, sous-dimensionnements, problèmes terre |
| 📊 Dimensionnement tableau | ✅ Complété | Tableau 3×13 modules, 24 utilisés, 15 libres |
| 📍 Emplacement tableau | ✅ Décidé | Garage, hauteur 110-150 cm |
| 📏 Métré câbles | ✅ Complété | Métré initial ~40m, ajusté sur chantier |
| 🛠️ Achat matériel | 🚧 En cours | Câbles 3G1,5 et 3G2,5 achetés ; goulottes et coffret tableau achetés |
| 🔧 Installation | 🚧 En cours | P5/P6 recâblés en prises sécurisées + 3G2,5mm² (55m tirés), raccordement en attente d’amenée au nouveau tableau |
| ✔️ Tests et validation | ⏳ À réaliser | Checklist préparée |

### Journal de chantier

**09/03/2026**
- Reprise du câblage des circuits **P5** et **P6** avec nouvelles prises sécurisées.
- Tirage réalisé en **3G2,5 mm²** jusqu'au nouveau tableau.
- Longueur totale de câble utilisée : **55 m**.
- Achat de **50 m de 3G1,5 mm²**.
- **Nouveau tableau fixé au mur**.
- **Goulottes fixées au mur**.
- Conducteurs **phase/neutre 2,5 mm²** récupérés pour réemploi prévu sur la liaison ancien tableau bas → nouveau tableau bas.
- **P5 et P6 non reliés** à ce stade : amenée d'électricité au nouveau tableau non encore réalisée.

---

## Résumé

Ce projet a pour objectif de spécifier et planifier le remplacement d'un tableau électrique domestique par un nouveau tableau, en respectant la norme NF C 15-100.

## Contexte

On constate des courants de fuite importants sur le neutre de certains circuits. Le remplacement doit être réalisé avec un minimum de coupure de courant pour l'utilisateur.

## Objectifs

- Inventorier l'installation existante (plans, circuits, équipements).
- Identifier les points de vigilance et les problèmes (fuites de courant, dimensionnement incorrect, etc.).
- Dimensionner le nouveau tableau et définir les protections nécessaires pour chaque circuit.
- Lister le matériel et la procédure de raccordement des anciens circuits au nouveau tableau.

## Contenu du dépôt

### Données
- `data/installation.yaml` : inventaire complet de l'installation (circuits, équipements, protections)

### Documentation
- Plans généraux:
	- [RdC — Plan](doc/plans_etage/Rdc-Page-1.svg) ([Édition](doc/plans_etage/Rdc.drawio))
	- [Étage — Plan](doc/plans_etage/Etage-Page-1.svg) ([Édition](doc/plans_etage/Etage.drawio))
- Plans électriques:
	- [RdC — Plan électrique](doc/plans_etage/Rdc_elec-Rdc-Elec.svg) ([Édition](doc/plans_etage/Rdc_elec.drawio))
	- [Étage — Plan électrique](doc/plans_etage/Etage_elec-Etage-Elec.svg) ([Édition](doc/plans_etage/Etage_elec.drawio))
- Schéma unifilaire:
	- [Schéma unifilaire du tableau](doc/schema_unifilaire_tableau-Schéma-Unifilaire.svg) ([Édition](doc/schema_unifilaire_tableau.drawio))
- Documents principaux:
	- [doc/proposition_tableau_electrique.md](doc/proposition_tableau_electrique.md) : **✅ RÉALISÉ** - **référentiel technique maître** (architecture, conformité, dimensionnement, coûts)
	- [doc/plan_implantation_tableau.md](doc/plan_implantation_tableau.md) : **✅ RÉALISÉ** - **mode opératoire d'implantation** (positionnement physique, cheminement, checklist)
	- [doc/plan_organisation_tableau.md](doc/plan_organisation_tableau.md) : **✅ RÉALISÉ** - **mode opératoire d'organisation interne** (répartition, procédure, contrôles)
	- [doc/etiquettes_tableau.md](doc/etiquettes_tableau.md) : **✅ RÉALISÉ** - étiquettes A4 imprimables pour repérage des circuits et fils
	- [doc/metré_rallonges_cables.md](doc/metré_rallonges_cables.md) : **✅ RÉALISÉ** - calcul des longueurs de câbles nécessaires et devis matériel
	- [doc/checklist_validation.md](doc/checklist_validation.md) : checklist de validation post-remplacement

## Gouvernance documentaire

### Règles de référence

1. **Source maître unique** : [doc/proposition_tableau_electrique.md](doc/proposition_tableau_electrique.md)
   - Toute décision technique (NF C 15-100, calibres, sections, logique énergétique, coûts) est maintenue ici.
2. **Documents opératoires** :
   - [doc/plan_implantation_tableau.md](doc/plan_implantation_tableau.md) pour l'implantation physique terrain.
   - [doc/plan_organisation_tableau.md](doc/plan_organisation_tableau.md) pour l'exécution chantier et l'organisation interne.
3. **Règle d'arbitrage** : en cas d'écart entre documents, la proposition technique fait foi.
4. **Anti-duplication** : ne pas recopier de tableaux de dimensionnement/coûts dans les modes opératoires ; utiliser un renvoi vers la proposition.
5. **Mise à jour coordonnée** : toute modification d'architecture dans la proposition doit entraîner une vérification des deux plans opératoires et de [doc/checklist_validation.md](doc/checklist_validation.md).

### Photos
- [Tableau buanderie (fermé)](doc/tableau_buanderie.jpg)
- [Tableau buanderie (ouvert)](doc/tableau_buanderie_ouvert.jpg)
- [Sous-tableau étage (fermé)](doc/tableau_etage.jpg)
- [Sous-tableau étage (ouvert)](doc/tableau_etage_ouvert.jpg)

## Structure recommandée du README

1. ✅ Résumé
2. ✅ Contexte
3. ✅ Objectifs
4. ✅ Inventaire de l'installation
5. ✅ Analyse et points de vigilance
6. ✅ Dimensionnement du nouveau tableau
7. ✅ Procédure de remplacement
8. ⏳ Tests et validation (à compléter après installation)
9. ✅ Contribution
10. ✅ Licence

## Inventaire de l'installation

**✅ RÉALISÉ** - Voir [data/installation.yaml](data/installation.yaml)

Inventaire complet des 14 circuits (8 au RdC, 6 à l'étage) avec équipements, sections de câbles, calibres de disjoncteurs et défauts identifiés.

**Plans** : [RdC](doc/plans_etage/Rdc-Page-1.svg) ([Édition](doc/plans_etage/Rdc.drawio)) | [RdC Élec](doc/plans_etage/Rdc_elec-Rdc-Elec.svg) ([Édition](doc/plans_etage/Rdc_elec.drawio)) | [Étage](doc/plans_etage/Etage-Page-1.svg) ([Édition](doc/plans_etage/Etage.drawio)) | [Étage Élec](doc/plans_etage/Etage_elec-Etage-Elec.svg) ([Édition](doc/plans_etage/Etage_elec.drawio))

**Photos** : [Tableau buanderie](doc/tableau_buanderie.jpg) | [Tableau buanderie ouvert](doc/tableau_buanderie_ouvert.jpg) | [Tableau étage](doc/tableau_etage.jpg) | [Tableau étage ouvert](doc/tableau_etage_ouvert.jpg)

## Analyse et points de vigilance

**✅ RÉALISÉ** - Voir [data/installation.yaml](data/installation.yaml) et [proposition_tableau_electrique.md](doc/proposition_tableau_electrique.md)

Identification des courants de fuite, sous-dimensionnements, défauts d'isolement et non-conformités. Analyse des contraintes de service et des distances réglementaires NF C 15-100.

## Dimensionnement du nouveau tableau

**✅ RÉALISÉ** - Voir [proposition_tableau_electrique.md](doc/proposition_tableau_electrique.md)

Tableau 3 rangées × 13 modules (24 utilisés, 15 libres). Architecture avec 3 interrupteurs différentiels (2× Type A, 1× Type AC) et répartition des circuits optimisée pour minimiser les modifications. Les circuits étage sont conservés et intégrés directement au tableau principal (suppression du sous-tableau étage).

**Schéma unifilaire** : [schema_unifilaire_tableau-Schéma-Unifilaire.svg](doc/schema_unifilaire_tableau-Schéma-Unifilaire.svg) ([Édition](doc/schema_unifilaire_tableau.drawio))

### Emplacement du nouveau tableau

**✅ RÉALISÉ** - Voir [plan_implantation_tableau.md](doc/plan_implantation_tableau.md)

Solution retenue : **garage**, hauteur 110-150 cm (conforme NF C 15-100, évite la chaleur de la chaudière).

## Procédure de remplacement

**✅ RÉALISÉ** - Voir [metré_rallonges_cables.md](doc/metré_rallonges_cables.md)

Liste complète du matériel nécessaire avec scénario tableau principal unique et métrés détaillés (liaisons étage directes de 10 m).

### Démarche

1. **Préparation** : Matériel, plan de coupure minimisée, consignation
2. **Installation rallonges** : circuits RdC + 6 circuits étage en liaison directe (10m)
3. **Coupure progressive** : Bascule des circuits non critiques
4. **Raccordement** : Connexion et étiquetage
5. **Tests et validation** : Isolement, mise sous tension progressive, validation fonctionnelle

## Modélisation des données

**✅ RÉALISÉ** - Format YAML adopté : [installation.yaml](data/installation.yaml)

Structure de données complète incluant circuits, équipements, sections, protections et défauts. Format lisible, versionnable et exploitable pour calculs.

**Outils utilisés** : Draw.io (plans et schémas), YAML (données), Markdown (documentation)

## Tests et validation

**⏳ À COMPLÉTER** après installation

Tests prévus : mesures d'isolement, contrôle différentiels, continuité des terres, validation conformité NF C 15-100.

**Checklist** : [checklist_validation.md](doc/checklist_validation.md)

## Contribuer

- Ouvrir une issue pour toute modification proposée.
- Fournir plans, photos et mesures ajoutées dans les dossiers `doc/` et `data/`.

## Licence

MIT

## Contact

Pierre Leduc
