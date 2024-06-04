# Gestion d'écrans LCD en temps réel avec FreeRTOS

## Résumé du Projet :
Ce projet implémente un système temps réel utilisant des écrans LCD ainsi que des capteurs de luminosité et de mouvement. Dans un premier temps, le système gère l'affichage sur trois écrans LCD en fonction de la luminosité ambiante et ensuite détecte les mouvements pour activer un message d'urgence.

Un capteur de luminosité mesure l'intensité lumineuse. Si la luminosité dépasse le seuil défini, SEUIL_LUMINOSITE, le système considère qu'il fait jour et envoie cet événement à la queue. En revanche, si la luminosité est inférieure au seuil, le système éteint les écrans LCD.

En ce qui concerne les écrans LCD, trois sont utilisés pour afficher des informations. Ainsi, lorsque la luminosité indique qu'il fait jour, un message "TV ALLUMEE" est affiché sur les écrans pendant une durée définie par un timer. Après cette durée, les écrans s'éteignent automatiquement.

De plus, un capteur de mouvement détecte toute présence dans la zone. Dès qu'un mouvement est détecté, un message d'urgence est affiché sur l'écran 1.

Enfin, le projet utilise FreeRTOS pour gérer les différentes tâches telles que la lecture de la luminosité, la gestion des écrans et la détection de mouvement de manière concurrente. Pour ce faire, chaque tâche s'exécute sur un cœur spécifique du microcontrôleur.

## Lien vers la Simulation :
[Lien vers Wokwi](https://wokwi.com/projects/399720113308033025)

## Membres du Groupe :
- KABORE Aronn
- SERE Akram
- ZIDA Eben-Ezer
- ZOUGOU Daniel
