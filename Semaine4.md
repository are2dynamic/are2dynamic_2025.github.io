## Compte rendu de la semaine 4 ##

Nous avons enfin réussi à mettre en place une fonction deplacement fonctionnelle. Nous avons également développé la fonction cycle, qui permet d'exécuter plusieurs déplacements des agents, ainsi qu'une fonction simulation pour visualiser l’évolution en temps réel.

Bien qu’on ait réussi à obtenir un modèle semi-fonctionnel, il ne correspond pas totalement à ce qu’on avait en tête au départ. En effet, même si les agents se déplacent, leurs mouvements ne sont pas optimisés. Parfois, ils font des déplacements inutiles, ce qui ralentit l’ensemble du processus. Au bout de plusieurs cycles, la plupart des agents arrivent à l'« endpoint », mais cela prend souvent trop de temps.

Ce manque d'efficacité est devenu un problème majeur, car il ralentit la performance globale de la simulation. On a vite compris qu’il nous fallait un algorithme de recherche de chemin plus avancé, comme l’algorithme A*, pour rendre le modèle plus efficace et permettre aux agents de se déplacer de manière plus intelligente. Cependant, avec le temps qui presse et notre manque d'expertise pour mettre en place cet algorithme, on a dû revoir nos plan.

Il ne nous reste plus que trois semaines avant la soumission du projet, alors on a décidé de réajuster notre approche. On va se concentrer sur la modélisation du comportement des piétons, notamment comment ils traversent la rue. Ce changement nous permet de simplifier les déplacements des agents et d’adapter nos fonctions existantes à ce nouveau modèle. Même si ça a demandé des ajustements rapides, on espère que ce réajustement nous permettra d’arriver à un résultat plus satisfaisant.
