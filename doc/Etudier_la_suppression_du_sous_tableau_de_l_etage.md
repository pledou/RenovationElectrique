# Étude de suppression du sous-tableau de l'étage

## Date
17 février 2026

## Objectif
Étudier la suppression du sous-tableau étage et le rattachement direct des circuits étage au tableau principal du garage, en cohérence avec toute la documentation existante.

## Base documentaire reprise
- `doc/proposition_tableau_electrique.md`
- `doc/plan_organisation_tableau.md`
- `doc/plan_implantation_tableau.md`
- `doc/metré_rallonges_cables.md`
- `doc/checklist_validation.md`

---

## Point 1 — Faisabilité technique (déjà validé)

### Données terrain validées
- Distance utile entre l'emplacement du sous-tableau étage et le futur tableau principal : **10 m**.
- Passage possible avec **seul un agrandissement de trou dans le parpaing en combles** si nécessaire.

### Conclusion point 1
La suppression du sous-tableau est **techniquement faisable** avec un cheminement direct vers le tableau principal.

---

## Point 2 — Impact budgétaire (analyse consolidée)

## Référence budgétaire existante
Le budget documentaire actuel (scénario avec sous-tableau conservé/remplacé) est de :
- **497 € TTC estimés sans outillage**
- **547 € TTC estimés avec outillage**

Référence : `doc/metré_rallonges_cables.md`.

## Effets économiques de la suppression du sous-tableau

### Économies attendues
- Suppression du **coffret étage 13 modules**.
- Suppression des accessoires dédiés au sous-tableau (partie boîtes/raccords spécifique étage).
- Suppression des opérations de pose/repose du sous-tableau (temps d'intervention réduit sur l'étage).

### Surcoûts attendus
- Rallonges directes des circuits étage jusqu'au tableau principal avec base de distance **10 m**.
- Longueurs de câbles supplémentaires en **3G1,5 mm²** (VMI, L3, L4) et **3G2,5 mm²** (P5, P6, P7).
- Petite fourniture/mise en œuvre pour l'**agrandissement ponctuel du passage en parpaing** (combles).

## Ordre de grandeur consolidé
À partir des prix unitaires et postes déjà présents dans `doc/metré_rallonges_cables.md` :
- l'économie liée à la dépose du sous-tableau est **partiellement compensée** par l'augmentation de longueur des câbles de liaison directe,
- l'impact net est **faiblement favorable à la suppression**, avec un budget global attendu **proche ou légèrement inférieur** au scénario de référence.

### Position budgétaire retenue
- **Hypothèse prudente** : budget total similaire au scénario actuel (écart modéré).
- **Hypothèse optimisée** : légère baisse du coût total si le passage combles reste simple (agrandissement minimal).

---

## Point 3 — Modifications matérielles (liste complète)

## Principe de modification
Remplacer l'architecture « tableau principal + sous-tableau étage » par une architecture « tableau principal unique ».

## Éléments retirés
- Sous-tableau étage (coffret divisionnaire).
- Liaison dédiée d'alimentation du sous-tableau (logique de tableau divisionnaire).
- Accessoires associés au coffret étage (support, borniers/peigne dédiés, habillage local).

## Éléments conservés
- Les **6 circuits étage existants** (VMI, P5, L3, L4, P6, P7).
- Les disjoncteurs réutilisables déjà documentés.
- L'implantation du tableau principal en garage.

## Éléments ajoutés / adaptés
- Rallongement direct des 6 circuits étage vers le tableau principal (base de parcours : 10 m).
- Reprise des raccordements et repérages selon `doc/etiquettes_tableau.md`.
- Ajustement du passage en combles : agrandissement local du trou parpaing si besoin.

## Impacts documentaires sur les autres fichiers

### `doc/proposition_tableau_electrique.md`
- Supprimer la section de remplacement du sous-tableau étage.
- Rebasculer les circuits VMI/P5/L3/L4/P6/P7 dans le périmètre du tableau principal.

### `doc/plan_organisation_tableau.md`
- Retirer le circuit d'alimentation `st_etage` en tant que départ vers sous-tableau.
- Réaffecter les 6 circuits étage sur les emplacements libres du tableau principal.
- Mettre à jour la logique de repérage des départs.

### `doc/metré_rallonges_cables.md`
- Remplacer la logique « rallonge locale sous-tableau » par « liaison directe 10 m » pour les 6 circuits étage.
- Recalculer les quantités de 3G1,5 mm² et 3G2,5 mm².

### `doc/checklist_validation.md`
- Ajouter des points de contrôle sur les nouvelles liaisons directes étage → tableau principal.
- Ajouter un contrôle spécifique du passage combles (protection mécanique, finition du trou).

---

## Point 4 — Capacité du tableau principal

## État de référence
Selon `doc/plan_organisation_tableau.md` :
- Tableau principal : **3 rangées × 13 modules = 39 modules**.
- Utilisés : **21 modules**.
- Libres : **18 modules**.

## Effet de suppression du sous-tableau
- Le départ `st_etage` (1 module disjoncteur) n'est plus utilisé comme alimentation de tableau divisionnaire.
- Les 6 circuits étage deviennent des départs directs au tableau principal (**+6 modules**).

### Bilan modules
- Variation nette : **+5 modules**.
- Nouvel utilisé estimé : **26 modules**.
- Modules restants estimés : **13 modules libres**.

## Conclusion capacité
- Le tableau principal reste **suffisamment dimensionné**.
- **Aucune 4ème rangée n'est nécessaire** dans cette configuration.
- Une marge de réserve significative est conservée pour extensions futures.

---

## Recommandation finale

La suppression du sous-tableau étage est **recommandable** sous réserve des conditions déjà validées :
- cheminement direct confirmé (10 m),
- agrandissement local du passage en combles maîtrisé,
- mise à jour documentaire complète des schémas, métrés, implantation interne et checklist.

Cette option simplifie l'architecture (tableau principal unique), maintient la capacité du tableau principal sans 4ème rangée, et reste budgétairement cohérente avec les estimations existantes.