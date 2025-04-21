# LES CROISEMENTS AUX PASSAGES PIÈTON

### Compte rendu de la Semaine 3 

L’objectif principal du projet est d’assurer que les agents naviguent dans l’environnement pour atteindre un point d’arrivée désigné. Pour cela, nous avons développé plusieurs fonctions, basées sur les résultats des étapes précédentes.

La fonction deplacement_possible détermine les directions possibles dans lesquelles un agent peut se déplacer (N, S, E, O) en fonction de sa position actuelle. Elle simule ainsi la prise de décision de l'agent pour trouver son chemin.

Nous avons également développé la fonction cul_de_sac, qui identifie lorsque l’agent est bloqué par des obstacles. Dans ce cas, l’agent est "condamné", ce qui signifie qu’il ne pourra plus progresser. Cette position devient alors un obstacle pour les autres agents.

La fonction position_agent nous permet de suivre la position des agents en temps réel, en veillant à ce qu’ils ne se superposent pas.

Nous avons aussi mis en place la fonction init_biais, qui attribue un biais aléatoire à chaque agent. Ce biais influence son comportement et rend la simulation plus dynamique en introduisant de la variabilité dans la manière dont chaque agent se déplace vers son objectif.

François avait déjà préparé un code partiel pour l'animation, ce qui constitue un progrès notable. Cependant, cette animation nécessite encore quelques ajustements pour intégrer correctement la fonction deplacement et refléter en temps réel l’évolution des positions des agents.

Malheureusement, nous avons rencontré des difficultés avec certaines fonctions de déplacement, ce qui a ralenti notre progression. Ces problèmes ont introduit des complications imprévues qu’il nous faudra résoudre pour pouvoir avancer correctement.
