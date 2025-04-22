# LES CROISEMENTS AUX PASSAGES PIÈTON

### Compte rendu de la semaine 6 

Dans notre dernière mise à jour, nous avons ajouté plusieurs nouvelles fonctions pour améliorer le fonctionnement et les performances de notre modèle. Voici les principales :

#### search_line:
Cette fonction permet de repérer le point d’arrivée d’une ligne ainsi que la position des feux de signalisation qui s’y trouvent. Elle fonctionne un peu comme notre ancienne coor_endpoint, mais en plus complet. Grâce à elle, le déplacement des véhicules et des piétons est plus fluide, avec des transitions mieux gérées.

#### search_passage:
Elle renvoie les coordonnées des limites du passage piéton, ce qui nous permet de bien définir les zones réservées aux piétons dans la simulation.

#### upd_traffic_lights: 
Comme son nom l’indique, cette fonction met à jour l’état des feux de circulation, en s’adaptant au flux de trafic en temps réel.

Nous avons aussi modifié certaines fonctions importantes :

#### deplacement_possible:
Nous y avons intégré de nouvelles conditions et variables pour rendre les calculs plus précis sur la possibilité de se déplacer ou non.

#### deplacement_voitures:
C’est une nouvelle fonction que nous avons créée pour gérer les déplacements des véhicules, en respectant certaines règles.

#### position_agents est maintenant devenue *position_type. Elle a été modifiée pour renvoyer la position des agents en fonction de leur type (véhicule, piéton…).

#### deplacement:
le fonction, qui gère les déplacements de manière générale, a été modifiée pour intégrer la nouvelle logique. Mais on rencontre encore un problème : les piétons d’un côté de la simulation ne bougent pas comme prévu. C’est encore un défi qu’il nous reste à résoudre avant la fin.

Enfin, les fonctions cycle et simulation ont été ajustées afin que l’ensemble du système fonctionne bien avec les nouvelles fonctions et variables mises en place. Nous sommes proches de la fin du projet, mais tant que le problème de déplacement des piétons n’est pas résolu, il reste un point critique. On espère y arriver cette semaine pour pouvoir tout boucler dans les temps !
