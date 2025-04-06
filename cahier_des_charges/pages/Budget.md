# Budget

### **Railway (ancien outil)**

>N'est plus utiliser (cf nouvelle plateforme utilisée "Fly.io")

Pour Railway et dans le cadre du projet nous allons utiliser l’abonnement **Hobby** à 5$ par mois avec les 5$ offerts par mois. Tous les services bénéficient de 8 GB RAM et 8 vCPU.

Dans un cadre réel et pour bénéficier de machines plus puissantes et de régions, le déploiement en prod devrait être fait sur l’abonnement **Pro** à 20$ par mois et par utilisateur. Tous les services auraient bénéficier de 32 GB RAM et 32 vCPU.

Les couts sur Railway dépendent de l’usage. Pour réduire les couts il est possible d’activer l’app sleeping à des 
ressources, ce qui permet de les mettre en veille lorsqu’elle ne sont pas utilisées.

Les ressources en dev seront en auto sleep. 

---

### **Fly.io**

>Nouvelle plateforme utilisée 

Les abonnements possibles :

| offre | CPU (core) | RAM | type | usage | prix |
| --- | --- | --- | --- | --- | --- |
| 1 | 1 | 1 GB | shared | moyenne/haute | 5.70 $ |
| 2 | 2 | 1 GB | shared | moyenne/haute | 6.39 $ |
| 3 | 2 | 2 GB | shared | moyenne/haute | 11.39 $ |
| 4 | 2 | 4 GB | shared | moyenne/haute | 21.40 $ |
| 5 | 4 | 4 GB | shared | moyenne/haute | 22.78 $ |

Le choix de l'abonnement pour l'hébergement de notre application se porte sur l'abonnement à 22.78 $ par mois;
En effet cette offre comprend plusieurs éléments qui cadre correctement avec nos besoins,    

---

### **Supabase**

Pour Supabase et dans le cadre du projet nous allons utiliser l’abonnement gratuit (à vérifier et tester). Nous allons l’utiliser pour stocker les utilisateurs, les données de l’application et les embeddings du backend ia.

 

Les deux abonnements bénéficient de :

| abonnement | utilisateurs mensuels | stockage database | stockage fichiers | bandwidth | Backup journaliers |
| --- | --- | --- | --- | --- | --- |
| gratuit | 50,000 | 500 MB | 1 GB | 5 GB | non |
| pro | 100,000 | 8 GB | 100 GB | 250 GB | oui |

---

### **Groq**

Pour Groq et notre accès aux IA, nous allons utiliser l’abonnement gratuit. L’abonnement à l’usage n’est pas encore disponible.

Nos limites actuelles sont de :

| modèle | requêtes par minute | requêtes par jours | tokens par minute |
| --- | --- | --- | --- |
| gemma-7b-it | 30 | 14,400 | 15,000 |
| llama3-8b-8192 | 30 | 14,400 | 30,000 |
| llama3-70b-8192 | 30 | 14,400 | 6,000 |
| mixtral-8x7b-32768 | 30 | 14,400 | 5,000 |
