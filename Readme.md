# Renovation Electrique

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

- `Readme.md` : documentation et guide de structure (ce fichier).
- `data/` : fichier(s) de modélisation de l'installation (voir section suivante).
- `doc/` : plans, schémas unifilaires, photos et exports SVG/PNG.

## Structure recommandée du README

1. Résumé
2. Contexte
3. Objectifs
4. Inventaire de l'installation
5. Analyse et points de vigilance
6. Dimensionnement du nouveau tableau
7. Procédure de remplacement
8. Tests et validation
9. Contribution
10. Licence

## Inventaire de l'installation (à remplir)

- Plan de l'installation (emplacement du tableau, pièces desservies).
- Liste des circuits : nom, fonction, section des conducteurs, calibre du disjoncteur, longueur estimée.
- Équipements présents (chauffe-eau, four, plaque, chauffage, etc.).
- Mesures relevées (fuites, résistances d'isolement, intensités mesurées).

## Analyse et points de vigilance

- Circuits présentant des courants de fuite sur le neutre : localisation et hypothèses causes.
- Circuits surdimensionnés ou sous-dimensionnés.
- Contraintes d'interruption de service (pièces critiques, horaires à éviter).

## Dimensionnement du nouveau tableau

- Nombre de modules requis, répartition des rangées.
- Protections différentielles et disjoncteurs recommandés (types et calibres).
- Schéma unifilaire proposé (fichier `doc/schema_unifilaire.svg` ou `doc/schema_unifilaire.drawio`).

## Procédure de remplacement (résumé)

1. Préparation : liste du matériel, plan de coupure minimisée, matériel de consignation.
2. Coupure progressive et bascule des circuits non critiques.
3. Raccordement et étiquetage des circuits sur le nouveau tableau.
4. Tests d'isolement et mise sous tension progressive.
5. Validation fonctionnelle et restitution à l'utilisateur.

## Modélisation des données et outils (suggestions)

- Format de stockage recommandé : `data/installation.json` ou `data/installation.yaml` contenant :
	- `circuits` : tableau d'objets {`id`, `nom`, `fonction`, `section`, `disjoncteur`, `longueur_m`, `notes`}.
	- `plans` : liste de chemins vers les fichiers dans `doc/`.
- Avantages : format lisible, versionnable, facile à exploiter pour calculs ou générateurs de schémas.

- Outils et extensions VS Code utiles :
	- YAML / JSON validators
	- PlantUML ou Draw.io pour schémas unifilaires
	- Extensions de gestion d'images et de previews SVG

## Tests et validation

- Procédures de test après installation : mesures d'isolement, contrôle des différentielles, tests de continuité et de mise à la terre.
- Checklist de validation à compléter dans `doc/checklist_validation.md`.

## Contribuer

- Ouvrir une issue pour toute modification proposée.
- Fournir plans, photos et mesures ajoutées dans les dossiers `doc/` et `data/`.

## Licence

MIT

## Contact

Pierre Leduc
