# LES CROISEMENTS AUX PASSAGES PIÈTON

![cpp](https://github.com/user-attachments/assets/67459fe5-8457-4bfc-a443-3049f7916baa)

# DESCRIPTION DU PROJET #
Les passages piétons sont des points dans lesquels se rencontrent beaucoup de foules. Ces mouvements de foule qui se passent au quotidien sont pourtant paramétrés par différents facteurs. Nous allons donc tenter de les représenter dans le but de mieux comprendre les diverses interactions qui y ont lieu. Pour représenter au mieux ces comportements, nous allons faire varier différents paramètres permettant de simuler plusieurs situations. Nous allons aborder ce sujet du point de vue suivant :

                                          + Comment se comporte-t-on aux passages piétons?
                                                       
                                                       
Avec l'objectif pour simuler les comportements piétonnier afin d'améliorer la circulation

## Le Terrain 

Pour simplifier le passage piéton, nous avons choisi de les représenter par des matrices avec des passages piétons horizontaux qui laissent juste assez d'espace en haut et en bas pour qu'on y fasse apparaître des voitures.

Les voitures, représentées par des carrés 2x2, sont les seuls obstacles que les agents rencontreront sur le terrain mis à part eux-mêmes. Elles se déplacent dans l'axe vertical, vont deux fois plus vite qu'un agent et respectent les feux rouges.

Sur le terrain, on retrouve également la délimitation des passages piétons représentée par deux lignes verticales qui alternent entre rouge et vert pour imiter la signalisation que les piétons rencontrent sur un passage piéton.

Les agents sont représentés par des couleurs claires (bleu et orange), ils ont pour but d'atteindre la rive opposée du passage piéton représentée par des couleurs plus foncées (bleu et orange). Ainsi, les agents bleu clair iront vers la rive bleu foncé, et il en est de même pour les agents orange et la rive orange foncée.

### Les principaux éléments : 

Sur le terrain, les foules rencontreront :
  + Des obstacles :
    + Feux tricolores
    + Passage piétons
    + Des voitures

### Des objectifs :

+ Points de départs/d'arrivées

+ Traverser sans risque

## Un terrain toujours plus grand (20x20, 50x50, 100x100,...)


# Algorithmes de déplacement :
## Biais 
Afin de simuler des comportements, nous avons implémenté un système de biais à nos agents dans le but d'ajouter des interactions non seulement entre les agents mais aussi entre les agents et leur environnement (voiture, feux tricolores) :

+ Direct : Il s'agit d'un comportement "normal", les agents ayant ce biais n'ont jamais de problèmes quand ils rencontrent un agent d'un autre type.

+ Prudent : Il agit comme le biais "Direct", sauf que les agents de ce type font très attention aux voitures et laisseront passer une voiture.

+ Imprudent : Il agit comme le biais "Direct", sauf que les agents de ce type ne font pas attention aux voitures et peuvent être victimes d'accidents.

+ Confus : Lorsqu'un agent Confus rencontre un autre agent Confus, les deux agents restent sur place pour un cycle avant de se passer. Lorsqu'un agent Confus rencontre un agent Brutal, ils échangent de places mais l'agent Confus reste sur place pendant un cycle.

+ Brutal : Lorsqu'un agent Brutal rencontre un autre agent Brutal, ils échangent de place et sont étourdis après leur altercation pendant un cycle.

## Voiture :

Les voitures sont générées en haut du passage piéton et se déplacent de 2 cases vers le bas chaque cycle. Elles sortent du terrain si leurs déplacements les mènent en dehors du terrain.

Elles ne passeront pas sur le passage piéton, si elles n'y sont pas déjà, lorsque c'est au tour des piétons de passer. Si elles sont sur le passage piéton, elles continueront d'avancer peu importe la signalisation jusqu'à éventuellement sortir du terrain. Toutefois, elles éviteront d'écraser les piétons du mieux qu'elles le peuvent.

Si un piéton passe devant elles, elles ne bougeront pas. Mais si elles peuvent se déplacer avant d'avoir le piéton en face, elles se déplaceront pour s'arrêter juste devant le piéton qui bloque leur chemin.

Toutefois, des accidents peuvent tout de même survenir, mais uniquement lors d'une rencontre entre un agent imprudent et une voiture. L'accident sera représenté par une case blanche sur le terrain et agit comme un obstacle pendant un cycle, puis sera enlevée au cycle suivant.



# Membres Du Groupe:

#### Simon Chen. 
+ simon.chen@etu.sorbonne-universite.fr

#### François Alicante. 
+ francois_alicante@etu.sorbonne-universite.fr

#### Qianqian Yang. 
+ qianqian.yang@etu.sorbonne-universite.fr

#### George Baiye.
+ george_kum.baiye@etu.sorbonne-universite.fr

## COMPTE RENDU: ##

[Semaine 1](https://are2dynamic.github.io/are2dynamic_2025.github.io/Semaine1)  

[Semaine 2](https://are2dynamic.github.io/are2dynamic_2025.github.io/Semaine2)

[Semaine 3](https://are2dynamic.github.io/are2dynamic_2025.github.io/Semaine3)

[Semaine 4](https://are2dynamic.github.io/are2dynamic_2025.github.io/Semaine4)

[Semaine 5](https://are2dynamic.github.io/are2dynamic_2025.github.io/Semaine5)

[Semaine 6](https://are2dynamic.github.io/are2dynamic_2025.github.io/Semaine6)

[Semaine 7](https://are2dynamic.github.io/are2dynamic_2025.github.io/Semaine7)
