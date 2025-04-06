# Gestion des risques

### **Qualité et intégrité des données**

Il y a un risque de données inexactes ou incomplètes.

Nous allons établir des scripts de tests et de préparations des données. Nous allons aussi évaluer les réponses de l'IA en fonctionne de différents documents.

> Utilisation de sources gouvernementales

> Séparation logiques des données, automatisation de la préparation des données via des scripts.

---

### **Dérive du modèle IA**

Notre modèle risque d’être obsolète ou moins précis avec le temps.

Nous allons mettre à jour les documents régulièrement, et pourrons facilement mettre à jour le modèle Groq utilisé.

---

### **Confidentialité et sécurité des données**

Il y a un risque de fuite de données utilisateurs et de leurs documents.

Nous allons encrypter les données sensibles des utilisateurs. Pour ce qui est de leurs documents, nous ne pouvons pas les encrypter, mais nous pouvons filtrer les données que l’on sauvegarde. Nous allons aussi nous assurer que l’accès à la database reste le plus sécurisé possible.

> Accès stricte aux documents

> Aucun filtrage des données, cela pourrait engendrer une perte de données lors des recherches.

---

### **Conformité aux lois et réglementations**

Il faut que nos pipelines et stockages de donnés soient et restent conformes aux réglementations en vigueur (RGPD, FINRA…)

> Suppression de toutes les données (documents, conversations...) automatique à la fermeture du compte

---

### **Problèmes techniques**

Il y a un risque de défaillances techniques.

Nous allons mettre en place des tests sur les routes pour nous s’assurer que les applications soient bien opérationnel. Nous aurons aussi la possibilité de rollback vers une version d’un service plus stable. Nous auront aussi la possibilité de faire des backup de nos databases.

---

### **Extensibilité (scalability)**

Il y a un risque de surcharge de nos applications frontend, backend et IA.

Nous utiliserons Railway pour l’hébergement de nos applications. Nos services seront scalables verticalement et horizontalement.

> Nous utilisons désormait Fly.io, mais les avantages s'appliques aussi.

> Un downtime cours voir inéxistant lors de la mise à jours des machines.

Nous pourrons aussi utiliser l’abonnement on-demand sur Groq pour bénéficier d’un accès complet aux modèles et sans limites.