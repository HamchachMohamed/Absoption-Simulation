# Simulation d'une Colonne d'Absorption - DWSIM

## Description du Projet

Ce projet présente la simulation d'une colonne d'absorption pour la purification d'un flux d'azote contaminé par de l'acétone, utilisant l'eau comme solvant d'absorption. La simulation a été réalisée avec le logiciel open-source DWSIM.

## Objectif

Traiter un flux gazeux d'azote contaminé par de l'acétone pour obtenir un gaz épuré répondant aux spécifications industrielles, avec un objectif de réduction de l'acétone à moins de 0,8% en fraction molaire.

## Configuration du Procédé

### Équipement
- **Type** : Colonne d'absorption à plateaux
- **Nombre d'étages** : 4 et 12 (étude comparative)
- **Configuration** : Contre-courant
- **Modèle thermodynamique** : NRTL
- **Algorithme de convergence** : Burningham-Otto
- **Tolérance** : 1E-05

### Conditions Opératoires
- **Pression** : 1,01325 bar (atmosphérique)
- **Espacement des plateaux** : 0,5 m
- **Température d'alimentation gaz** : 30°C
- **Température d'alimentation eau** : 25°C

## Flux d'Alimentation

### Gaz Contaminé (Entrée)
- **Débit** : 200 kg/h
- **Composition** :
  - Acétone : 11,5% (fraction molaire)
  - Azote : 88,5% (fraction molaire)

### Solvant d'Absorption
- **Type** : Eau pure
- **Débit** : 1000 kg/h
- **Composition** : 100% H₂O

## Résultats de Simulation

### Performance de Base (4 étages)

**Gaz Épuré (Lean Gas)**
- Acétone : 0,485% (fraction molaire)
- Eau : 3,17%
- Azote : 96,35%
- **Efficacité d'absorption** : Modérée

**Eau Riche (Rich Water)**
- Acétone : 1,26% (fraction molaire)
- Eau : 98,74%

### Performance Optimale (12 étages)

**Gaz Épuré (Lean Gas)**
- Acétone : 0,00415% (fraction molaire)
- Eau : 3,13%
- Azote : 96,86%
- **Efficacité d'absorption** : 99,964%

**Eau Riche (Rich Water)**
- Acétone : 1,30% (fraction molaire)
- Eau : 98,70%
- **Débit de sortie** : 1039,33 kg/h

### Analyse Comparative par Nombre d'Étages

| Étages | Acétone dans le gaz (%) | Acétone dans l'eau (%) | Efficacité |
|--------|-------------------------|------------------------|------------|
| 4      | 0,485                   | 1,26                   | Modérée    |
| 12     | 0,00415                 | 1,30                   | 99,964%    |

**Impact du dimensionnement** : Le passage de 4 à 12 étages réduit la teneur en acétone du gaz de 99,1%, démontrant l'importance cruciale du nombre d'étages théoriques.

## Logiciel Utilisé

**DWSIM** - Simulateur de procédés chimiques open-source
- Version : Dernière version stable
- Avantages : Gratuit, fiable, interface utilisateur intuitive
- Modèles thermodynamiques : NRTL pour systèmes polaires

## Applications Industrielles

Ce procédé trouve des applications dans :
- Industrie pharmaceutique
- Industrie chimique
- Fabrication de peintures et solvants
- Récupération de COV (Composés Organiques Volatils)
- Traitement d'effluents gazeux avant rejet atmosphérique

## Conclusions

La simulation démontre :
1. **Sur-performance** : Résultats 99,5% supérieurs à l'objectif initial
2. **Optimisation réussie** : 12 étages offrent le meilleur compromis efficacité/coût
3. **Validité du modèle** : NRTL approprié pour le système eau-acétone-azote
4. **Faisabilité technique** : Procédé viable pour applications industrielles

## Perspectives d'Amélioration

- Optimisation économique du ratio solvant/gaz
- Étude de sensibilité aux variations opératoires
- Évaluation de la récupération d'acétone par distillation
- Analyse du cycle de vie et impact environnemental

## Auteur

Simulation réalisée dans le cadre d'un projet d'ingénierie des procédés, démontrant l'utilisation de logiciels open-source pour le dimensionnement d'équipements industriels.
