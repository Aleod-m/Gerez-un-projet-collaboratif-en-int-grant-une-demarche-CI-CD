# Document explicatif.

## Les Workflows

Il y a 4 workflows différents présent dans le répertoire.

Le workflow TEST fais tourner les TEST automatiquement quand une PR est ouverte
ou quand on pousse des commit sur la branche master.

Si le workflow TEST fini avec un statut de succès le workflow REPORT crée un
rapport visualisable dans l'onglet actions.

En parallèle le workflow SONAR fait tourner sonar sur le code et charge les
résultats dans SonarCloud.

Si les workflows TEST est SONAR finissent avec succès le workflow DEPLOY se
lance et déploie les images sur DockerHub.

Pour accéder aux service distant ces workflow utilisent des secrets:
- `DOCKERHUB_USERNAME`: login de connexion a DockerHub.
- `DOCKERHUB_TOKEN`: token utilisé a la connexion.
- `SONAR_TOKEN_FRONT`: token utilisé pour charger le scan dans SonarCloud.
- `SONAR_TOKEN_BACK` token utilisé pour charger le scan dans SonarCloud.

## Les KPI (Key Performance Indicators)

Les KPI sont un peu différents des seuils a respecter. C'est plus des
indicateur pour mesurer la performance/efficacité d'une équipe de
développement, plutôt que des indicateur pour mesurer la qualité du code. On
peut y retrouver la fréquence de déploiement le temps de "build", le
pourcentage de changement provoquant des échecs en production.

Mais je pense qu'un "test coverage" entre 70 et 90 % est une bonne chose. Et
peut être ajouter des "quality gates" dans sonar en particulier sur la sécurité
et la maintenabilité de sonar pourrais être intéressantes.

## Avis Utilisateurs

D'après les avis utilisateurs une fonctionnalité permettant de suggérer des
blagues pourrais être intéressante. Ainsi que peut être un système de vote.
