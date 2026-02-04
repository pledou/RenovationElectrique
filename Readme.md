# Renovation Electrique

## État d'avancement du projet

**Dernière mise à jour** : 4 février 2026

| Phase | État | Détails |
|-------|------|---------|
| 📋 Inventaire installation | ✅ Complété | `data/installation.yaml` - 14 circuits identifiés |
| 📐 Plans et schémas | ✅ Complétés | Plans RdC/Étage + schéma unifilaire |
| 🔍 Analyse défauts | ✅ Complétée | Fuites, sous-dimensionnements, problèmes terre |
| 📊 Dimensionnement tableau | ✅ Complété | Tableau 3×13 modules, 21 utilisés, 18 libres |
| 📍 Emplacement tableau | ✅ Décidé | Garage, hauteur 110-150 cm |
| 📏 Métré câbles | ✅ Complété | ~40m de câbles nécessaires, devis établi |
| 🛠️ Achat matériel | ⏳ À réaliser | Liste complète disponible |
| 🔧 Installation | ⏳ À réaliser | Procédure documentée |
| ✔️ Tests et validation | ⏳ À réaliser | Checklist préparée |

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
- `doc/Rdc.drawio` : plan du rez-de-chaussée
- `doc/Etage.drawio` : plan de l'étage
- `doc/schema_unifilaire_tableau.drawio` : schéma unifilaire du tableau
- `doc/proposition_tableau_electrique.md` : **✅ RÉALISÉ** - proposition détaillée du nouveau tableau (architecture 3 rangées, dimensionnement, protections)
- `doc/plan_implantation_tableau.md` : **✅ RÉALISÉ** - étude comparative des emplacements possibles pour le nouveau tableau
- `doc/metré_rallonges_cables.md` : **✅ RÉALISÉ** - calcul des longueurs de câbles nécessaires et devis matériel
- `doc/checklist_validation.md` : checklist de validation post-remplacement

### Photos
- `doc/tableau_buanderie.jpg` : photo du tableau actuel buanderie (fermé)
- `doc/tableau_buanderie_ouvert.jpg` : photo du tableau actuel buanderie (ouvert)
- `doc/tableau_etage.jpg` : photo du sous-tableau étage (fermé)
- `doc/tableau_etage_ouvert.jpg` : photo du sous-tableau étage (ouvert)

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

**Plans** : [RdC](doc/Rdc.drawio) | [Étage](doc/Etage.drawio)

**Photos** : [Tableau buanderie](doc/tableau_buanderie.jpg) | [Tableau buanderie ouvert](doc/tableau_buanderie_ouvert.jpg) | [Tableau étage](doc/tableau_etage.jpg) | [Tableau étage ouvert](doc/tableau_etage_ouvert.jpg)

## Analyse et points de vigilance

**✅ RÉALISÉ** - Voir [data/installation.yaml](data/installation.yaml) et [proposition_tableau_electrique.md](doc/proposition_tableau_electrique.md)

Identification des courants de fuite, sous-dimensionnements, défauts d'isolement et non-conformités. Analyse des contraintes de service et des distances réglementaires NF C 15-100.

## Dimensionnement du nouveau tableau

**✅ RÉALISÉ** - Voir [proposition_tableau_electrique.md](doc/proposition_tableau_electrique.md)

Tableau 3 rangées × 13 modules (21 utilisés, 18 libres). Architecture avec 3 interrupteurs différentiels (2× Type A, 1× Type AC) et répartition des circuits optimisée pour minimiser les modifications. Le sous-tableau étage est conservé.

**Schéma unifilaire** : [schema_unifilaire_tableau.drawio](doc/schema_unifilaire_tableau.drawio)

### Emplacement du nouveau tableau

**✅ RÉALISÉ** - Voir [plan_implantation_tableau.md](doc/plan_implantation_tableau.md)

Solution retenue : **garage**, hauteur 110-150 cm (conforme NF C 15-100, évite la chaleur de la chaudière).

## Procédure de remplacement

**✅ RÉALISÉ** - Voir [metré_rallonges_cables.md](doc/metré_rallonges_cables.md)

Liste complète du matériel nécessaire (~40m de câbles multiconducteurs, protections différentielles, disjoncteurs) avec métrés détaillés et devis.

### Démarche

1. **Préparation** : Matériel, plan de coupure minimisée, consignation
2. **Installation rallonges** : 9 circuits à rallonger (3m par circuit)
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
