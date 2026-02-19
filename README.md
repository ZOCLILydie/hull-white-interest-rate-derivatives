# Valorisation de produits dérivés de taux – Modèle de Hull-White

## Présentation

Ce projet implémente la valorisation de produits dérivés de taux d’intérêt sous le modèle de Hull-White à un facteur. Le modèle est calibré sur la courbe initiale des taux via l’ajustement Nelson-Siegel.

## Dynamique du modèle

La dynamique du taux court est donnée par :

dr(t) = (θ(t) - a r(t)) dt + σ dW(t)

Le terme θ(t) est déterminé afin de reproduire parfaitement 
la structure initiale des taux.

## Éléments implémentés

### Calibration de la courbe des taux
- Téléchargement de la courbe ECB
- Calibration Nelson-Siegel
- Calcul du taux forward instantané

### Modèle de Hull-White
- Solution analytique du taux court
- Pricing d’obligations zéro-coupon
- Changement de mesure vers la T-forward measure

### Produits dérivés valorisés
- Swap plain vanilla
- Cap (Monte Carlo)
- Cap (formule fermée)
- Swaption européenne (Monte Carlo)
- Swaption bermudéenne (Least-Squares Monte Carlo)

## Paramètres utilisés

r0 = 3%  
a = 0.1  
σ = 1%

## Outils

Python :
- numpy
- pandas
- scipy
- matplotlib

## Auteur

Lydie ZOCLI  
Master 2 Modélisation Financière - Centrale Méditerranée et Aix-Marseille School of Economics
