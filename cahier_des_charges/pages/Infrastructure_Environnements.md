# Infrastructure Environnements

### **dev**

Utilisation de :
- variables d’environnements de tests
- une branche dev
- un projet Supabase free dev
- machines dev
- déploiement et lancement des tests automatique

Cet environnement a pour but de faire les derniers correctifs et tests avant la mise en production. Les résultats des tests unitaires n’empêchent pas la déploiement dans l’environnement.

---

### **production**

Utilisation de :
- variables d’environnements production
- une branche main
- un projet Supabase pro prod
- machines prod
- déploiement auto après tests

Cet environnement correspond à la mise en production. Les tests unitaires doivent tous passer pour que les ressources soient déployées.

---

Un rollback vers un déploiement passé est possible.