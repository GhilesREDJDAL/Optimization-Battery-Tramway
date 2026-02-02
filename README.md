# Multi-Objective Optimization: Tramway Energy Storage System

Ce projet porte sur la conception optimale d'un systeme de stockage d'energie par batterie embarque pour un tramway. L'objectif principal est de maximiser la recuperation d'energie lors du freinage afin de stabiliser la tension du reseau electrique et de reduire les pics de consommation.

## Problematique d'Optimisation

Le dimensionnement repose sur la recherche d'un compromis entre deux objectifs contradictoires :
1. Minimisation de la capacite de la batterie : Reduction des couts de production, du poids embarque et de l'encombrement.
2. Minimisation de la chute de tension maximale : Amelioration de la robustesse de l'alimentation electrique pour eviter d'atteindre les limites critiques du systeme.

## Architecture du Projet

Le projet est divise en trois etapes cles :

### 1. Modelisation du Systeme
Implementation des lois physiques regissant le reseau ferroviaire (Lois de Kirchhoff et d'Ohm). Le modele calcule en temps reel les resistances de ligne (LAC et rails) en fonction de la position du tramway pour simuler les chutes de tension et les flux de puissance.

### 2. Exploration par Methode de Monte-Carlo
Echantillonnage aleatoire de l'espace des decisions (Capacite vs Seuil de puissance). Cette approche permet d'identifier la topologie de l'espace des objectifs et de construire un premier front de Pareto pour comparer les solutions initiales.

### 3. Optimisation par Algorithme Genetique (NSGA-II)
Mise en oeuvre des concepts fondamentaux de l'algorithme NSGA-II (Nondominated Sorting Genetic Algorithm II). L'utilisation d'operateurs de selection, de croisement et de mutation permet une convergence efficace vers un front de Pareto optimal, offrant un meilleur panel de solutions techniques.

## Competences Techniques Demontrees
- Optimisation Multicritere : Maitrise de la dominance de Pareto et des solutions non dominees.
- Intelligence Calculatoire : Developpement et ajustement d'algorithmes evolutionnaires.
- Simulation Energetique : Modelisation de flux de puissance et de systemes de stockage.
- Langages et Outils : Python, NumPy, Matplotlib, Jupyter Notebook.

## Resultats Visuels

### Front de Pareto Final
Le graphique ci-dessous illustre le compromis optimal entre la capacite de stockage et la qualite de la tension reseau.
![Front de Pareto](pareto_results.png)

### Profil de Puissance
Analyse temporelle des echanges energetiques entre le train, la batterie et le reseau.
![Profil Energetique](power_profile.png)

---
Projet realise dans le cadre du Master de Sorbonne Universite (2024-2025).
