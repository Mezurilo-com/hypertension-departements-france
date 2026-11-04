# Hypertension traitée, diabète et facteurs territoriaux par département (France métropolitaine)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23941352.svg)](https://doi.org/10.5281/zenodo.23941352)
[![Licence: CC BY 4.0](https://img.shields.io/badge/licence-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

*English: 96-row open dataset (one metropolitan French département per row) comparing the share of people treated for hypertension (ages 55-59 and 20-24, 2024) with treated diabetes, temperature, polluted sites, water hardness, access to cardiologists, poverty rate and population density. Column descriptions below are in French.*

Jeu de données archivé sur Zenodo : https://doi.org/10.5281/zenodo.23941352

Tableau de 96 lignes (un département de France métropolitaine par ligne) qui rapproche le taux de personnes
traitées pour hypertension de huit autres indicateurs issus de sources ouvertes. Il accompagne l'étude
« Hypertension par département : la France coupée en deux » publiée par Mezurilo :
https://www.mezurilo.com/blogs/guides-des-tensiometres/hypertension-par-departement

Fichier : `hypertension-departements-france-2024.csv` (UTF-8, séparateur virgule, point décimal, codes département en texte : `01`, `2A`, `2B`).

## Colonnes

| Colonne | Contenu | Unité | Source | Année |
|---|---|---|---|---|
| `code_departement` | code INSEE du département | texte | | |
| `departement` | nom du département | texte | | |
| `hypertension_traitee_55_59_ans_pct` | part des 55-59 ans traités par antihypertenseurs, hors patients ayant une autre pathologie prise en compte (diabète, maladie cardiaque, etc.) | % | Assurance Maladie (CNAM), cartographie des pathologies, indicateur `TFC_HTA_EXC` | 2024 |
| `hypertension_traitee_20_24_ans_pct` | même indicateur pour les 20-24 ans | % | idem | 2024 |
| `diabete_traite_55_59_ans_pct` | part des 55-59 ans pris en charge pour diabète | % | CNAM, indicateur `DIA_CAT_CAT` | 2024 |
| `temperature_moyenne_c` | température moyenne annuelle du département, moyenne pondérée par la population des communes | °C | Météo-France (SAFRAN), via choisirsaville.fr | normales 2015-2025 |
| `sites_pollues_basol_pour_100000_hab` | sites et sols pollués recensés, rapportés à la population | sites pour 100 000 hab. | Base des sols pollués (BASOL), ministère de la Transition écologique | 2024 |
| `durete_eau_degres_francais` | dureté de l'eau du robinet (titre hydrotimétrique) | °f | Ministère de la Santé, contrôle sanitaire de l'eau (SISE-Eaux) | 2023 |
| `acces_cardiologues_apl` | accessibilité potentielle localisée aux cardiologues, moyenne départementale pondérée par la population | indice IRDES | IRDES, APL Cardiologie | 2019 |
| `taux_pauvrete_pct` | taux de pauvreté monétaire (seuil à 60 % du niveau de vie médian) | % | INSEE, Filosofi (`PR_MD60`) | 2023 |
| `densite_hab_km2` | densité de population | hab./km² | INSEE (data.gouv.fr) | 2022 |

Les arrondis sont ceux du fichier de travail (1 à 3 décimales selon la colonne). Les valeurs ne sont pas modifiées
au-delà de l'arrondi.

## Périmètre et limites

- France métropolitaine uniquement (96 départements, Corse comprise). Les départements d'outre-mer sont exclus :
  les profils d'âge et de prise en charge diffèrent fortement (Mayotte tirait les corrélations vers le haut).
- L'indicateur d'hypertension mesure des **personnes traitées**, pas la prévalence réelle de la maladie. Il dépend
  aussi du dépistage et de l'accès aux soins. Il exclut les patients dont l'hypertension est comptée avec une autre pathologie.
- Les comparaisons sont faites à âge égal (tranches de 5 ans). Le classement tous âges confondus reflète surtout l'âge moyen du département.
- Les millésimes diffèrent selon les colonnes (de 2019 à 2024).
- Ces données décrivent des départements, pas des individus : une corrélation entre départements ne dit rien sur la cause chez une personne.

## Résultats principaux (55-59 ans, 96 départements)

- Écart maximal : 22,8 % dans le Pas-de-Calais contre 12,0 % dans les Hautes-Alpes. À 20-24 ans, l'écart atteint un facteur 3.
- Corrélation (Pearson) avec l'hypertension traitée à 55-59 ans : diabète +0,69 ; température -0,41 ; dureté de l'eau +0,37 ;
  sites pollués +0,33 ; accès aux cardiologues -0,26 ; densité -0,14 ; taux de pauvreté ≈ 0.
- Une corrélation n'établit pas de cause.

## Reproduction

Les données brutes sont ouvertes :
- Cartographie des pathologies : https://www.data.gouv.fr/datasets/62b31f7b128643f46ea1f848/
- Base des sols pollués : https://www.data.gouv.fr/datasets/5d4dd16c6f444161e140abc9/
- Niveau de vie et taux de pauvreté : https://www.data.gouv.fr/datasets/687ae011ddfd9c43eb553747/
- Densité de population : https://www.data.gouv.fr/datasets/69b98949748e7142f7dbfbe9/
- APL Cardiologie (IRDES) : https://www.data.gouv.fr/datasets/69e144dca6801ac0ad0f4655/

## Licence et citation

Compilation publiée par Mezurilo sous licence CC BY 4.0. Les données d'origine restent soumises aux licences de leurs
producteurs (en général la Licence Ouverte 2.0 d'Etalab) : citer les sources ci-dessus.

Citation suggérée : Mezurilo (2026). *Hypertension traitée, diabète et facteurs territoriaux par département
(France métropolitaine)*. Zenodo.
