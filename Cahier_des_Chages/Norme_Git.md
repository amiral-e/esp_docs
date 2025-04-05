# Norme Git

### **Gestion des repos et branches**

Le projet est constituer de 3 repos, frontend, backend et backend ia.

Chaque repo aura des branches dev et main, ainsi que des branches pour chaque feature à implémenter.

**main :** 

Cette Branche correspond à la mise en production. Les tests unitaires doivent tous passer pour que les merges request soient déployées sur cette branche.

**dev** :

Cette branche a pour but de faire les derniers correctifs et tests avant la mise en production. Les résultats des tests unitaires n’empêchent pas la déploiement dans l’environnement. Elle sert aussi de point de départ pour tout les autres branches crées.

**x :**

Cette branche a pour but d’implémenter une nouvelle fonctionnalité, cette branche est crée via la branche dev. Une fois que l’implémentation est faite elle est ensuite testé fonctionnellement et avec des tests unitaires, on peut alors lancer un pull request vers dev pour une revue du code.
Son nom correspond à l'issue linear à laquelle elle répond, cela permet l'automatisation du changement de status des tickets via les actions GitHub.

---

### Collaboration (pull requests, code reviews...)

**Méthode :**

- Créer une branche feature-x avec comme base la branche dev puis faire une pull request vers la branche dev une fois que le code et les tests sont commits.
- Corriger les bugs et faire les tests finaux de la branche dev; apres un certains nombres de features et si la brance dev est stable, faire une pull request vers la branche main.

---

### Norme commits

**Commit :**

- <type> : <message>

**Type :**

| type | description |
| --- | --- |
| build | changes that affect the build system or external dependencies (example scopes: npm, pip) |
| docs | documentation only changes |
| feat | a new feature |
| update | a code/feature update |
| fix | a bug fix |
| test | adding tests or correcting existing tests |
| perf | a code change that improves performance |
| style | changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, typo, etc) |

**Langue :**

- Les commits et pull requests en français
- Les notes, tasks et descriptions dans linear en français

**Linear :**

Le linear a été mis à jour et peut désormais être utilisé. Les tâches concernant le cahier des charges et le mvp ont été instancié.