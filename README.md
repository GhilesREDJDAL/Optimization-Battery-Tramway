# Optimisation Multicriteres du Stockage d Energie : Tramway et Reseau de Distribution

Ce projet porte sur la modelisation et l optimisation d un systeme de stockage embarque pour un tramway circulant sur une ligne alimentee par une sous-station. L objectif est de gerer les flux d energie pour minimiser l impact sur le reseau electrique.

## Modelisation du Systeme Electrique

Le modele developpe simule l interaction entre plusieurs composants cles :
- Le reseau de distribution : Modelisation de la Ligne Aerienne de Contact (LAC) et du retour par les rails.
- La sous-station : Source de tension avec une resistance interne specifique.
- La charge mobile : Le tramway, dont la position et la puissance varient selon un profil de marche reel.
- Le stockage embarque : Une batterie controlee pour recuperer l energie de freinage et limiter les pointes de courant.

## Problematique de l Optimisation

Le projet resout le compromis entre deux objectifs antagonistes identifies dans l etude :
1. Minimisation de la capacite de la batterie : Reduction de la masse embarquee et du cout systeme.
2. Minimisation de la chute de tension maximale : Maintien de la tension aux bornes du tramway au-dessus des limites critiques lors des phases de traction forte.

## Methodologie et Algorithmes

### Modelisation et Simulation Temporelle
Calcul iteratif de la tension au pantographe en fonction de la distance a la sous-station et de l etat de charge de la batterie. Le modele integre egalement la dissipation d energie dans le rheostat de freinage lorsque le stockage est sature.

### Exploration par Methode de Monte-Carlo
Realisation d un echantillonnage aleatoire sur les variables de decision (Capacite et Seuil de puissance) pour identifier la topologie de l espace des solutions.

### Optimisation par Algorithme NSGA-II
Implementation de l algorithme genetique NSGA-II pour converger vers le Front de Pareto. Cette etape permet d identifier les configurations optimales garantissant une stabilite du reseau avec un stockage minimal.

## Environnement de Developpement
- Langage : Python
- Biblioteques : NumPy, Matplotlib
- Outils : Jupyter Notebook

---
Projet realise dans le cadre de l unite MU4MEN01 - Sorbonne Universite (Session 2024-2025).
