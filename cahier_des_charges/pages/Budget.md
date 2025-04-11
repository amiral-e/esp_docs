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

| offre | CPU (core shared) | RAM | usage | prix (mois)| 
| --- | --- | --- | --- | --- |
| 1 | 1 | 512 MB | moyenne/haute | 3.19 $ |
| 2 | 1 | 1 GB | moyenne/haute | 5.70 $ |
| 3 | 2 | 1 GB | moyenne/haute | 6.39 $ |
| 4 | 2 | 2 GB | moyenne/haute | 11.39 $ |
| 5 | 2 | 4 GB | moyenne/haute | 21.40 $ |
| 6 | 4 | 4 GB | moyenne/haute | 22.78 $ |

Pour le backend, notre utilisation actuelle nous permet d'utiliser l'offre 1 mais pour prévenir d'une surcharge en cas de forte utilisation l'offre 2 nous semble plus adapté.    

Le frontend étant plus gourmand que le backend l'offre 1 ne suffit pas (les 512 MB de RAM ne sont pas suffisants). En cas de forte utilisation, pour prévenir d'une surcharge, il nous parait plus judicieux d'utiliser l'offre 4.

> surcharge : Augmentation du temps de réponse d'une machine 

Notre infrastructure se compose de :
- Backend :
    - 1 machine prod -> offre 2
    - 1 machine dev -> offre 1
- Frontend :
    - 1 machine prod -> offre 4
    - 1 machine dev -> offre 3

Les machines dev sont très peu utilisées étant donner quelles ont l'auto-sleep activer, nous estimons leurs coûts entre 10-15% de leurs prix.

Le budget moyen estimé (estimation haute) est de **18.53$**

>Calcul : 
(5.70$ + 3.19$*0.15) + (11.39$ + 6.39$*0.15) = (offre 2 + offre 1 * 15%) + (offre 4 + offre 3 * 15%) = (Backend) + (Frontend)


> Nous avons également la possibilité de scale la capacité de nos machines et/ou le nombres de machines pour répondre au mieux à l'évolution du nombre d'utilisateur de la plateforme 

---

### **Supabase**

Les abonnements possibles :

| abonnement | prix | utilisateurs mensuels | stockage database | stockage fichiers | bandwidth | Backup journaliers | Bonus
| --- | --- | --- | --- | --- | --- | --- | --- |
| gratuit | 0 $ | 50,000 | 500 MB | 1 GB | 5 GB | non | 0
| pro | 25$ | 100,000 | 8 GB | 100 GB | 250 GB | oui | 10$ compute

Le choix de l'abonnement pro nous permet d'avoir les capacités de croissance necessaire sur du moyen/long terme.

Notre infrastructure se compose de :
- 1 projet pro prod
- 1 projet free dev

Le budget moyen estimé est de 25$ (+10$ bonus compute).

> Le dépassement de l'usage entraine des frais supplémentaires

---

### **Groq**

Lors de nos tests et du développement, nous utilisons l'abonnement free de Groq.

Limites de nos modèles dans cet abonnement :

| modèle | requêtes par minute | requêtes par jours | tokens par minute | tokens par minute |
| --- | --- | --- | --- |  --- |
| llama-3.3-70b-versatile | 30 | 1,000 | 6,000 | 100,000 |

Pour la production, nous utilisons l'abonnement  développeur (pay as you go).

Voici les informations de nos modèles dans cet abonnement :

| modèle | Prix Input par 1M Token | Prix Output par 1M Token | Context Size
| --- | --- | --- | ---  |
| llama-3.3-70b-versatile | 0.59$ | 0.79$ | 128k

Le budget moyen est de ...

---

### **OpenAi**

Nous utilisons l'abonnement (pay as you go).

Les abonnements possibles :

| modèle | Prix par 1M Token |
| --- | --- |
| text-embedding-ada-002 | 0.10$ |

Le budget moyen est de ...

---

### **Stripe**

Nous utilisons l'abonnement standard.

Les abonnements possibles :

| abonnement | Prix par transaction |
| --- | --- |
| Offre standard | 1,5 % + 0,25 € |

> Le prix par transaction est défini pour les cartes standard de l'Espace économique européen.