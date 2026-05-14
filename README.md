# Détection de la Sévérité de l'Acné par Deep Learning

## Description

Classification automatique de la sévérité de l'acné en 4 niveaux à partir de photos de visages, via EfficientNet-B0
et une loss ordinale originale.

## Dataset

ACNE04 — 1457 images annotées par des dermatologues (Wu et al., ICCV 2019)

- Niveau 0 : Pas d'acné
- Niveau 1 : Légère
- Niveau 2 : Modérée
- Niveau 3 : Sévère

## Résultats

| Modèle                       | Accuracy | F1-Score |
| ---------------------------- | -------- | -------- |
| KNN (baseline)               | 44.8%    | 0.308    |
| CNN Scratch                  | 48.1%    | 0.344    |
| EfficientNet + Cross-Entropy | 64.8%    | 0.570    |
| EfficientNet + Loss Ordinale | 61.0%    | 0.526    |

## Originalité technique

Remplacement de la cross-entropy par une loss ordinale qui encode l'ordre des niveaux via 3 questions binaires.
