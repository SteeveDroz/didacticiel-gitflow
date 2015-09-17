# didacticiel-gitflow

Un didacticiel (ou tutoriel) expliquant le GitFlow.

# GitFlow

Le GitFlow est une architecture permettant de séparer le projet en branches distinctes, chaque branche possédant une utilité propre.

# Les branches

# master

La branche `master` est la branche principale. Cependant, c'est la moins utilisée de toutes : elle ne contient que les versions publiques. Un utilisateur n'ayant accès qu'à la branche `master` ne verra donc que les versions successives du logiciel en mode production, en aucun cas les versions de travail.

# dev

La branche `dev`, issue de la version de base de la branche `master`, est la version de travail. Tout ce qui se trouve dessus est terminé, il n'y a aucune modification en travail. C'est autour de cette branche que les développeurs travailleront le plus souvent, sans pour autant la modifier réellement.

# branches de travail

De la branche `dev` ou d'une branche de travail déjà existante, chaque développeur peut créer une branche de travail portant le nom de l'amélioration qu'il développe. Il est important de toujours garder à l'esprit qu'une branche concerne une amélioration.

Dans une branche d'amélioration, le travail peut être sauvegardé en cours de route, les commits de ces branches ne sont pas forcément sans erreurs.

# rc

Lorsqu'une version de la branche `dev` semble bonne à passer en production, on crée un embranchement de `dev` appelé `rc`. Quelques modifications peuvent encore avoir lieu afin de corriger les derniers problèmes et de gérer les différents aspects propres aux releases. Une fois que la branche est validée, elle peut être fusionnée avec la branche `master` et avec la branche `dev`. C'est la seule manière de modifier la branche `master`.
