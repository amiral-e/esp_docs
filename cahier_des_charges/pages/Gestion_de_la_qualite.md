# Gestion de la qualité

### **Stratégie**

La gestion de la qualité est un point primordial pour pouvoir garantir un suivi de projet claire et donner un support pour le respect des échéances au client.

Elle est également nécessaire pour permettre la conformité des spécificités du produit avec celles annoncées dans le cahier des charges.

La stratégie que nous avons adopté est la suivante :

- La décomposition du produit en “projets” (points clés de l’application) et tickets qui représentes les fonctionnalités détaillées (**Linear**)
- La définition d’échéances claires sous forme de roadmap, pour nos projets.
- La définition d’échéances claires pour nos tickets grâce aux cycles de 3 semaines.

- Des **Tests Unitaires p**our chaque fonctionnalité afin de vérifier que chaque composant fonctionne correctement
- Des **Tests de Performance** pour tester les performances de l'application sous différentes charges

- Nous allons utiliser des pipelines d'intégration et de déploiement continus (**CI/CD**) pour automatiser les tests et les déploiements, tout en s’assurant du déploiement de versions sans erreurs
- Nous allons tester les nouvelles versions dans un environnement de pré-production (dev) avant de les déployer en production (prod)

---

### **Tests et outils**

Pour garantir une meilleure stabilité lors du développement, nous mettrons en place une batterie de tests pour couvrir un maximum de coverage, qui seront exécutés à chaque merge vers la branche dev, conformément à la norme git. Cette démarche a pour objectif de détecter et corriger rapidement les potentielles régressions ou bugs introduits par les nouvelles modifications, avant même qu'elles n'atteignent l'environnement de production. En automatisant ces tests, nous nous assurons que chaque modification intégrée respecte les critères de qualité définis et maintient l'intégrité du projet.

En parallèle, nous allons intégrer l'outil [Bruno](https://www.usebruno.com/) pour créer et gérer une collection de routes. Cet outil nous permettra de centraliser et synchroniser nos tests des différentes routes sur les divers dépôts. En utilisant Bruno, nous faciliterons la cohérence et la couverture de nos tests, garantissant ainsi que toutes les routes sont rigoureusement vérifiées et fonctionnent comme prévu sur l'ensemble de nos environnements de développement et de production.

> Nous n'utilisons plus Bruno, nous testons les routes via la page /docs Scalar.

Pour assurer la stabilité de notre environnement de production, nous avons mis en place une procédure stricte de vérification des tests unitaires avant tout (re)déploiement de service. Concrètement, cela signifie qu'aucun service ne sera (re)déployé si un test unitaire échoue. Cette politique rigoureuse nous permet de prévenir les incidents en production et d'assurer une qualité constante des services déployés.

De plus, avant d'accepter une pull request, plusieurs étapes cruciales devront être respectées. Premièrement, une code review sera effectuée, impliquant plusieurs développeurs si nécessaire, pour garantir que le code respecte les standards de qualité et les bonnes pratiques. Ensuite, la norme du code sera vérifiée pour s'assurer qu'elle est conforme aux conventions établies. Enfin, la validation des tests unitaires devra être confirmée, garantissant que toutes les nouvelles fonctionnalités ou corrections n'introduisent pas de régressions.

Pour ce qui est du formatage du code TypeScript, nous utiliserons l'outil [Biome](https://biomejs.dev/). Biome nous aidera à maintenir un style de code cohérent et lisible à travers tout le projet, en automatisant le formatage selon les règles que nous avons définies. En standardisant le formatage du code, nous faciliterons la relecture et la maintenance du code, tout en réduisant les divergences stylistiques qui peuvent survenir dans un projet collaboratif.

En résumé, ces différentes mesures, allant de l'exécution systématique de tests à chaque merge à l'utilisation d'outils spécialisés pour la gestion des routes et le formatage du code, visent à améliorer la qualité, la stabilité et la cohérence de notre développement logiciel. Ces pratiques nous permettront non seulement de détecter et corriger rapidement les erreurs, mais aussi de garantir un déploiement fiable et sans interruption de nos services.

---

### **Frontend**

Au début du projet, l'interface utilisateur (UI) et l'expérience utilisateur (UX), ainsi que la structure des composants, seront définies de manière précise. Il est impératif que ces spécifications initiales soient rigoureusement respectées tout au long du développement jusqu'à la finalisation du projet. L'objectif principal de cette approche est de maintenir un code simple, ordonné et cohérent, ce qui facilitera non seulement la lecture et la maintenance du code, mais aussi la collaboration entre les différents membres de l'équipe.

---

### **Backend**

Pour assurer la validité des données entrantes et sortantes de nos routes, nous utiliserons la bibliothèque **Zod**. Cette bibliothèque permet de définir des schémas de validation stricts, garantissant que les données manipulées par notre API respectent les formats attendus. Chaque route de notre application sera conçue conformément aux spécifications **d'OpenAPI**, un standard bien établi pour la documentation et la description des API RESTful. En suivant ce format, nous  intégrerons **Swagger-UI**, un outil puissant qui offre une interface utilisateur interactive. Swagger-UI permettra non seulement de visualiser les différentes routes de notre API, mais aussi de les tester directement et de générer une documentation complète et à jour. Cette approche facilitera le développement, la maintenance et l'utilisation de notre API par les développeurs et autres parties prenantes.

> Zod n'est plus utilisé pour la vérification des inputs/outputs des routes.

> Swagger a été remplacé par Scalar

---

### **Backend IA**

Chaque route de notre application sera conçue conformément aux spécifications **d'OpenAPI**, un standard bien établi pour la documentation et la description des API RESTful. En suivant ce format, nous  intégrerons **Swagger-UI**, un outil puissant qui offre une interface utilisateur interactive. Swagger-UI permettra non seulement de visualiser les différentes routes de notre API, mais aussi de les tester directement et de générer une documentation complète et à jour. Cette approche facilitera le développement et la maintenance de notre API.

> Nous n'utilisons plus de backend ia, la logique a été implémenté directement dans le backend principal.

Pour garantir à la fois les performances et le degré de précision de notre système, nous procéderons à une évaluation rigoureuse des résultats produits par notre mécanisme de recherche, également appelé 'retriever'. Cette évaluation consistera à mesurer et analyser divers indicateurs de performance, tels que la rapidité des réponses, la pertinence des résultats, et d'autres métriques spécifiques à notre contexte d'utilisation. Une fois ces évaluations effectuées, il sera crucial d'intégrer ces processus d'évaluation dans notre pipeline d'intégration continue et de déploiement continu (CI/CD).

> Les système prompts ont été modifié de sorte à ce que l'assistant évite les documents erronés trouvés lors des recherches.

En incorporant ces évaluations dans notre pipeline CI/CD, nous pourrons automatiser le processus de validation. Concrètement, avant chaque déploiement vers l'environnement de production de notre backend IA, les résultats des évaluations serviront de critères pour décider si le déploiement peut se faire ou non. Cette automatisation assurera que seuls les versions du backend IA qui répondent à nos standards de performance et de précision atteignent la production, réduisant ainsi les risques de défaillances et améliorant la fiabilité globale de notre système.