# Return of Investment

## **Introduction**

Le Return on Investment (ROI) est un indicateur clé pour évaluer l'efficacité des investissements. Il mesure le rapport entre le bénéfice généré par notre projet ou une action et le coût initial engagé. En d'autres termes, le ROI permet de savoir si un investissement rapporte plus qu'il ne coûte, en exprimant ce résultat sous forme de pourcentage. Ce document présente une approche pratique pour calculer et optimiser le ROIs.

Avant toutes choses il est important de comprendre et de définir ce qui représente nos coût fixe qui sont défini dans la ressource [Buget](../cahier_des_charges/pages/Budget.md) et de calcul de nos **revenus bruts** et par la suite nos **revenus nets**. En effet sachant que notre application fait appel à des services externes payant qui sont facturer à l'utilisation, il est primordiale de connaitre et/ou estimer l'utilisation de chaque typologie d'utilisateur.   
 
---

## **Persona**

Ici nous allons definir trois persona qui sont trois typologie de client représentée par une personne fictive.

### Persona 1 : Camille — L’Étudiante en Droit

- **Âge** : 23 ans  
- **Statut** : Étudiante en Master 1 de droit des affaires  
- **Objectif** : Acquérir une base solide en comptabilité pour mieux comprendre les cas pratiques, les entreprises et le droit fiscal  
- **Fréquence d’usage** : occasionnelle (3-4 fois/mois)  
- **Fonctionnalités clés recherchées** :
  - Q&A pédagogiques illustrés avec des exemples
  - Glossaire juridique-comptable simplifié
  - Fiches synthétiques sur des notions clés (bilan, amortissements, comptes…)
- **Niveau technique/comptable** : Beginner


### Persona 2 : Mehdi — L’Auto-entrepreneur

- **Âge** : 34 ans  
- **Statut** : Graphiste freelance, micro-entreprise  
- **Objectif** : Gérer efficacement sa compta sans y passer trop de temps, comprendre ses obligations  
- **Fréquence d’usage** : Régulière (1–2 fois/semaine)  
- **Fonctionnalités clés recherchées** :
  - Explication de lignes comptables / seuils URSSAF
  - Vérification rapide de factures ou statuts fiscaux
  - Génération de mini-rapports ou fiches de suivi
- **Niveau technique/comptable** : Intermediate


### Persona 3 : Sophie — La Collaboratrice PME Opérationnelle

- **Âge** : 42 ans  
- **Statut** : Assistante administrative dans une PME (25 pers.)  
- **Objectif** : Gagner du temps dans le traitement des documents et échanges avec l’expert-comptable  
- **Fréquence d’usage** : Quotidienne  
- **Fonctionnalités clés recherchées** :
  - Analyse de documents (bilan, factures, fiches de paie)
  - Génération de rapports synthétiques pour la direction
  - Automatisation des contrôles simples (TVA, échéances)
- **Niveau technique/comptable** : Pro


**Nos personas et leurs besoins :** 

Ici les sont lister les besoins auxquels notre applications répond par typologie de client.

| cible | description | besoins |
| --- | --- | --- |
| particulier | utilise l'application dans le cadre de recherches personelles  | ingestion de documents, chat sur des documents et sur les connaissances de la plateforme, générations de rapports |
| autoentrepreneur | utilise l'application dans le cadre de ses activités professionelle (gestion, impôt, développement) | ingestion de documents, chat sur des documents et sur les connaissances de la plateforme, générations de rapports |
| PME |  utilise l'application dans le cadre de ses activités professionelle | chat sur les connaissances de la plateforme, chat sur les documents personel non soumis aux restrictions de l'entreprise, générations de rapports |

--- 

## **Etude de marché**

L'étude de marché vise à situer notre application dans un ecosystème déjà existant et nous permet de comparer notre offre et nos tarifs à nos concurent direct.

**Nos concurrents :** 

| plateform | fonctionnalité | offre (prix/mois)|
| --- | --- | --- |
| Humata | Ingestion et chat sur des documents | Expert 9.99 $ |
| Juribot | ChatIA (entrainer sur du droit) | offre personnalisée sur demande |
| sinao | Devis, Suivi des paiements, Facturation électronique, Déclaration et paiement TVA, Suivi financier | 11,40 € |
| LegiGPT | ChatIA (entrainer sur du droit)  | offre personnalisée sur demande |


**Outils comparables**

| Source / Plateforme | Infos disponibles sur les usages | Tarification estimée (€/mois ou €/action)|
|---|---|---|
| **ChatGPT usage logs** (via OpenAI et forums) | Moyenne de 10–20 prompts/jour pour les power users | 20 €/mois (ChatGPT Plus) / 0,002–0,01 € par prompt |
| **Sage, Pennylane, QuickBooks**| Onboarding + dashboards = 3–10 actions/document par session | 35 à 70 €/mois selon formule / ou 1–2 € par action analysée |
| **Notion AI, Jasper, Grammarly** | Moyenne de 1 document structuré généré par semaine chez les professionnels | 10 à 40 €/mois / ou 1 € par génération |
| **Zendesk / Intercom AI**  | 4–6 interactions/questions par session utilisateur (selon documentation UX) | 50 à 100 €/mois / ou 0,05 à 0,10 € par interaction |
| **UX benchmark IA métier** (Nielsen Norman Group) | 3–5 tâches répétées par utilisateur par session sur des outils spécialisés | Variable – extrapolation : 0,10 à 0,50 € par tâche |
    
---

## **Utilisations**

Ici l'objectif est de définir le fonctionnement des éléments payants de l'application, et de comprendre les différentes utilisations issue de nos typologie d'utilisateur.

### **Niveaux de connaissances**

 Tout d'abbord ComptaCompanion permet de choisir un niveau de connaissance qui correspond au format de retour de l'IA plus ou moins détaillé et complexe en fonction du niveau choisi par l'utilisateur.

| cible | niveau de connaissance |
| --- | --- |
| particulier | beginner/intermediate |
| autoentrepreneur | intermediate/pro |
| PME |  pro |

### **Questions prédéfinis**

ComptaCompanion propose également en fonction du niveau de connaissance des questions type accessible via le chat, qui nous permettent d'estimer "la charge de dialogue" entre un utilisateur et le modèle. 

***Question Beginner :*** 

1. "Quelle est la différence entre actif et passif ?"

2. "Comment calculer le seuil de rentabilité d’une entreprise ?"

3. "Quels sont les ratios financiers les plus utilisés ?"

4. "C’est quoi une écriture comptable d’amortissement ?"

***Question Intermediate :*** 

1. "Comment comptabiliser une variation de stock en fin d’exercice selon le PCG ?"

2. "Quelle est la méthode de calcul du coût de revient en comptabilité analytique ?"

3. "Comment interpréter un ratio d’endettement supérieur à 100 % dans une PME ?"

4. "Dans quel compte enregistre-t-on une charge constatée d’avance en comptabilité ?"

***Question Pro :*** 

1. "Comment comptabiliser une cession d'immobilisation avec une plus-value selon les règles fiscales françaises ?"

2. "Dans un rapprochement bancaire, comment traiter une écriture d’écart non justifiée datant de plus de 6 mois ?"

3. "Quels sont les impacts comptables d’un crédit-bail sur le bilan et le compte de résultat selon les normes IFRS 16 ?"

4. "Comment ventiler les charges indirectes dans une comptabilité analytique selon la méthode des centres d’analyse ?"

---

## **Utilsation estimer par typologie d'utilisateur** 

Un élement qu'il est important de noter est que les frais générés par notre commnication au modèle Groq sont relative aux nombres de tokens (1 token = 4 caractères) envoyé (Input) par l'utilisateur et renvoyé par le modèle (output)
(voir [Buget](../cahier_des_charges/pages/Budget.md))

Nous allons donc ici estimer des moyennes d'utilisation en nombre de caractères pour pouvoir ensuite les convertir en dollars.

### **Questions**

***Question Beginner :*** 

1. "Quelle est la différence entre actif et passif ?" → 48 caractères

2. "Comment calculer le seuil de rentabilité d’une entreprise ?" → 61 caractères

3. "Quels sont les ratios financiers les plus utilisés ?" → 50 caractères

4. "C’est quoi une écriture comptable d’amortissement ?" → 53 caractère

(48+61+50+53)/4 = 53 caractères par question en moyenne 

| Question | Taille estimée de la réponse |
|---|---|
| 1. Actif vs Passif | 200 caractères |
| 2. Seuil de rentabilité | 275 caractères |
| 3. Ratios financiers | 225 caractères |
| 4. Écriture d’amortissement | 250 caractères |

(200+275+225+250)/4 = 237 caractères par réponse en moyenne

***Question Intermediate :*** 

1. "Comment comptabiliser une variation de stock en fin d’exercice selon le PCG ?" → 84 caractères

2. "Quelle est la méthode de calcul du coût de revient en comptabilité analytique ?" → 84 caractères

3. "Comment interpréter un ratio d’endettement supérieur à 100 % dans une PME ?" → 91 caractères

4. "Dans quel compte enregistre-t-on une charge constatée d’avance en comptabilité ?" → 86 caractères

(84+84+91+86)/4 = 86 caractères par question en moyenne 

| Sujet | Taille estimée de la réponse |
|---|---|
| 1. Variation de stock selon le PCG | 300 caractères |
| 2. Calcul du coût de revient | 275 caractères |
| 3. Ratio d’endettement > 100 % | 300 caractères |
| 4. Charge constatée d’avance | 250 caractères |

(300+275+300+250)/4 = 281 caractères par réponse en moyenne 

***Question Pro :*** 

1. "Comment comptabiliser une cession d'immobilisation avec une plus-value selon les règles fiscales françaises ?"
-> 120 caractères

2. "Dans un rapprochement bancaire, comment traiter une écriture d’écart non justifiée datant de plus de 6 mois ?"
-> 125 caractères

3. "Quels sont les impacts comptables d’un crédit-bail sur le bilan et le compte de résultat selon les normes IFRS 16 ?"
-> 132 caractères

4. "Comment ventiler les charges indirectes dans une comptabilité analytique selon la méthode des centres d’analyse ?"
-> 122 caractères

(84+84+91+86)/4 = 124 caractères par question en moyenne 

| Sujet                                                                           | Taille estimée de la réponse |
|---------------------------------------------------------------------------------|------------------------------|
| 1. Cession d'immobilisation avec plus-value (règles fiscales FR)                   | 450 caractères               |
| 2. Traitement d’une écriture d’écart non justifiée dans un rapprochement bancaire  | 400 caractères               |
| 3. Crédit-bail et impacts comptables selon IFRS 16                                 | 500 caractères               |
| 4. Ventilation des charges indirectes par centre d’analyse (méthode analytique)    | 450 caractères               |
 

(400+450+500+400)/4 = 450 caractères par réponse en moyenne 

### **Ingéstion de documents**

Il faut également noter que nous utilisons pour OpenIA pour l'ingestion de document, le prix est également relatif au nombre de tokens envoyés (1 token = 4 caractères)  (voir [Buget](../cahier_des_charges/pages/Budget.md))

| Profil utilisateur | Type de documents ingérables                                  | Taille estimée (caractères) | Nombre moyen de caractères | Nombre estimé de pages |
|--------------------|---------------------------------------------------------------|-----------------------------|----------------------------|------------------------|
| Beginner           | Fiches pédagogiques, Q&A simplifiées, glossaires              | 1 000 à 3 000               | 2 000                      | 1 à 1.5 pages          |
| Intermédiaire      | Articles de blog spécialisés, extraits de manuels, cas simples| 3 000 à 6 000               | 4 500                      | 2 à 3 pages            |
| Pro                | Normes (PCG, IFRS), rapports financiers, procédures internes  | 6 000 à 15 000+             | 10 500                     | 5 à 7 pages            |

### **Génération de rapports**

La génération de rapports fonctionne de la même manière que le chat (groq) les tarrifications sont donc identitque (1 token = 4 caractères)  (voir [Buget](../cahier_des_charges/pages/Budget.md))

| Type de rapport généré                                    | Profil cible       | Taille estimée (caractères) | Taille moyenne estimée | Taille estimée (pages) |
|-----------------------------------------------------------|--------------------|-----------------------------|------------------------|------------------------|
| Résumé d’un document (synthèse simple)                    | Beginner           | 800 à 1 200                 | 1 000                  | 0.5 page               |
| Résumé explicatif ou reformulation pédagogique            | Intermédiaire      | 1 500 à 3 000               | 2 250                  | 1 à 1.5 pages          |
| Rapport d’analyse ou diagnostic comptable/financier       | Pro                | 3 000 à 6 000               | 4 500                  | 2 à 3 pages            |
| Rapport avec recommandations ou plan d’action             | Pro                | 5 000 à 10 000              | 7 500                  | 2.5 à 5 pages          |

### **Utilisation estimer global par typologie d'utilisateur**

| Profil utilisateur | Questions (caractères)        | Réponses (caractères)               | ingestion de documents (caractères) | génération de rapport (caractères) |
|--------------------|-------------------------------|-------------------------------------|-------------------------------------|------------------------------------|
| Beginner           | 53                            | 237                                 | 2 000                               | 1 000                              |
| Intermédiaire      | 86                            | 281                                 | 4 500                               | 2 250                              |
| Pro                | 574                           | 450                                 | 10 500                              | 6 000                              |

En supposant que la répartition des utilisateurs est uniforme nous avons :  
(Ici nous faisons la moyenne par fonctionalités)

| nombre total de caractères (questions)/mois | nombre total de caractères (réponses)/mois | nombre total de caractères (documents)/mois | nombre total de caactères (rapports)/mois |
|---------------------------------------------|--------------------------------------------|---------------------------------------------|-------------------------------------------|
| 238                                         | 323                                        | 5667                                      | 3084                                      |

Une fois le nombre de caractère par fonctionnalités et par typologie d'utilisateur estimé, il est important de réussir à comprendre la féquence d'utilisation pour nos trois persona. (source pour l'estimation en annexe)

| Typologie      | Questions posées/mois | Réponses générées/mois | Documents ingérés/mois | Rapports générés/mois |
|----------------|-----------------------|------------------------|------------------------|-----------------------|
| Beginner       | 80                    | 80                     | 2                      | 1.5                   |
| Intermédiaire  | 160                   | 160                    | 7.5                    | 6                     |
| Pro            | 300                   | 300                    | 22.5                   | 15                    |

En supposant que la répartition des utilisateurs est uniforme nous avons : 
(Ici est calculer la moyenne du nombres d'utilisations de chaque fonctionnalité)

| nombre total de questions posées/mois | nombre total de réponses générées/mois | nombre total de documents ingérés/mois | nombre total de rapports générés/mois |
|---------------------------------------|----------------------------------------|----------------------------------------|---------------------------------------|
| 180                                   | 180                                    | 11                                     | 7.5                                  |

Nous avons donc un total de caratères utilisés par mois par fonctionnalité : 
(ici nous muliplions la moyenne de caractères utlisés par fonctionnalité par la moyenne du nombre d'utilisation par fonctionnalité)

| nombre total de caractères(questions)/mois | nombre total de réponses générées/mois | nombre total de documents ingérés/mois | nombre total de rapports générés/mois |
|--------------------------------------------|----------------------------------------|----------------------------------------|---------------------------------------|
| 42 840                                    | 58 140                                | 62 337                                | 23 130                               |



---

## **Revenu estimé**

Ici il est primordiale de noter que les bénéfices de ComptaCompanion sont uniquement basés sur la marge faite par le'utilisations des fonctionalités 
Nous avons donc fixer des tarifications 100 fois suppérieur aux coût réel des réponses générés.

> Ici le coût de la génération de rapport est égale au coût d'une réponse, c'est à dire que l'on néglige les 1 à 10 phrases nécéssaire à la spécifications du contenu du rapport en comparaison des plusieurs page générées  

Le cout réel de l'utilisation des composants par les differentes fonctionnalitées sont les suivantes :

|Fonctionnalité|Entrée|Sortie|Traitement Document|Recherche|
|---|---|---|---|---|
|Chat|0.59$|0.79$|0|0|
|Chat Collection(s)|0.59$|0.79$|0|0.05$|
|Ingestion Document|0|0|0.10$|0|
|Génération Rapport|0|0.79$|0|0.05$|

On nottera ici que les tarification sont sur une référence de 1M de token soit 4 000 000 de caractères.

> *La génération de rapport envoie les documents fournis par l'utilisateur via l'Entrée. 

Le cout plateforme facturer à l'utilisateur pour l'utilisation des composants par les differentes fonctionnalitées sont les suivantes :

|Fonctionnalité|Entrée|Sortie|Traitement Document|Recherche|
|---|---|---|---|---|
|Chat|0.1475$|0.1975$|0|0|
|Chat Collection(s)|0.1475$|0.1975$|0|0.05$|
|Ingestion Document|0|0|0.025$|0|
|Génération Rapport|0|0.1975$|0|0.05$|

On nottera ici que les tarifications sont sur une référence de 10k caractères.

> *La génération de rapport envoie les documents fournis par l'utilisateur via l'Entrée. 

**Cout réel :**

Ce qui nous donne en multipliant le prix par l'utilisation estimer en nombre de caractères par fonctionnnalité par mois **pour un utilisateur**, le cout réel moyen d'un utilisateur par mois.

Ici il est important de noter que le chat collections represente la moitié de nos questions réponse mais intègre une recheche (search) dans le document pour emettre une réponse elle est donc inclus dans la tarification.

A noter ici que les quantité de caractère sont convertie en unité 10k caractères (1M token / 400).

Nous avons donc comme variable : 

- **Chat** = (Input_prix x nb_input + output_prix x nb_output) / 2

>(4.280 x 0.001475$ + 5.8140 x 0.001975$) / 2 = 0.0089$

- **chat collection** = ((Input_prix x nb_input + output_prix x nb_output) + (prix_search x (nb_input + nb_output)) / 2

>((4.280 x 0.001475$ + 5.8140 x 0.001975$) + (0.05$ x 10.09)) / 2 = 0.26$

- **ingestion** = prix_traitement x nb_docs

>6.2337 x 0.001975$ = 0.0123$

- **rapport** = (output_prix + prix_search) x nb_rapport

>(0.001975$ + 0.05$) x 2.3130 = 0.12$

total = 0.0089$ + 0.26$ + 0.0123$ + 0.12$ = 0.40$


**Cout plateforme :**

Ce qui nous donne en multipliant le prix par l'utilisation estimer en nombre de caractères par fonctionnnalité par mois, le cout réel d'un utilisateur par mois.


A noter ici que les quantité de caractère sont convertie en unité 10k caractères.

Nous avons donc comme variable : 

- **Chat** = (Input_prix x nb_input + output_prix x nb_output) / 2

>(4.280 x 0.1475$ + 5.8140 x 0.1975$) / 2 = 0.89$

- **chat collection** = ((Input_prix x nb_input + output_prix x nb_output) + (prix_search x (nb_input + nb_output)) / 2

>((4.280 x 0.1475$ + 5.8140 x 0.1975$) + (0.05$ x 10.09)) / 2 = 1.14$

- **ingestion** = prix_traitement x nb_docs

>6.2337 x 0.1975$ = 1.23$

- **rapport** = (output_prix + prix_search) x nb_rapport

>(0.1975$ + 0.05$) x 2.3130 = 0.57$

total = 0.89$ + 1.14$ + 1.23$ + 0.57$ = **3,83 $**


**Revenus généré :**

On a donc par la différence entre notre coût réel et le cout de la plateforme les revenus moyen généré par un utilisateur par mois.

**Revenus** = 3.83$ - 0.40$ = **3.43$** = **2.74€**

> Ici le taux de convertion Dollar américain vers euro est de 0.88.

---

## Seuil de rentabilité

### Composantes clés

| Élément                      | Description                                                        | Valeur |
|------------------------------|--------------------------------------------------------------------|--------|
| Charges fixes                | Coûts fixes totaux (par exemple : (hebergement, base de données))         |   36.39$ =  32.02€   |
| Prix de vente unitaire       | Prix de vente d'un produit ou service                              |  3.83$ = 2.74€   |
| Coût variable unitaire       | Coût variable pour produire une unité (ex : matières premières)   | aucun     |

> Ici le taux de convertion Dollar américain vers euro est de 0.88.

> Dans notre cas de figure nous excluons de potentiel salaire ou frais de location du bureau ici l'objectif est de comprendre le nombre de clients nécéssaire pour atteindre un seuil de rentabilité par rapport à nos frais de matériel (server et services)

### Calcul

Pour déterminer le nombre de client nécessaires pour atteindre le seuil de rentabilité (quantité à partir de laquel on génère des bénéfices), on utilise la formule suivante :

>Ici dans le prix de vente unitaire il ne faut pas négliger nos coût liée au paiement qui sont 1.5% + 0.25€ par transaction via notre application de paiement stripe (voir [Buget](../cahier_des_charges/pages/Budget.md))

On a donc : 

$$
\text{Prix de vente unitaire} = (2.74€ \times 0.985) - 0.25€ = \mathbf{2.45€}
$$

Ce qui nous donne : 
$$
\text{Seuil} = \frac{\text{Charges fixes}}{\text{Prix de vente unitaire} - \text{Coût variable unitaire}}
$$

$$
\text{Seuil} = \left( \frac{32.02}{2.45} \right) = 13.06
$$

**Il nous faut donc 14 clients pour atteindre notre seuil de rentabilité**

---

## Retour sur investissement 

Ici pour le ROI il serait possible de déterminer un nombre de client et de calculer le retour sur investissement par le revenus généré pour cette quantité, mais ce n'est pas ce que nous allons faire.
Sachant que le retour sur investissement dépend du nombre de client (avec une utilisation moyenne de la plateforme estimer à 1.80€ net par client) nous allons calculer le ROI par client.
**Cette méthode nous permet d'estimer le ROI en pourcetage et de le multiplie par le nombre de client pour avoir directement un ROI donné pour un nombre de client donné.**

### Composantes clés

| Élément | Description | valeur |
| --- | --- | --- |
| Coûts initiaux | Dépenses totales | 32.02€ |
| Revenus | Chiffre d’affaires ou bénéfices directs générés. | 2.74€ |
| Gain net | Revenus – Coûts (y compris coûts indirects). | 2.45 €|

---

### Calcul

$$
\text{ROI} = \left( \frac{\text{Gain net}}{\text{Coût initial}} \right) \times 100 = \left( \frac{\text{Revenus} - \text{Coûts}}{\text{Coûts}} \right) \times 100
$$

$$
\text{ROI} = \left( \frac{2.45}{32.02} \right) \times 100 = 7.65\%
$$

**Nous avons donc un retour sur investissement de 5.62% par client une fois le seuil de rentabilité atteint.**

**exemple : pour 100 clients** 
$$
\text{ROI} = \left( \frac{245}{32.02} \right) \times 100 = 765\%
$$

**exemple : pour 2 clients**
$$
\text{ROI} = \left( \frac{4.90}{32.02} \right) \times 100 = 15.30\%
$$

---

## Conclusion 

On peut conclure en remarquant que pour un tarif d'utilisation estimer **2.02€** par utilisateur par mois, **ComptaCompanion** est une plateforme concurrentielle par rapport au marché dans lequel elle s'inscrit (voir le chapitre "étude de marché").
De plus, le seuil de rentabilité est totalement accessible **14 clients** avec un retour sur investissement par client très élevé à partir du 19e client.   

---

## Annexes

### Camille – Étudiante en droit

| Fonctionnalité              | Source / Étude                                                         | Justification chiffrée                                                                 | URL                                              |
|-----------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| Q&A pédagogiques            | **Observatoire de la Vie Étudiante (OVE) – Enquête sur les conditions de vie des étudiant·e·s** | Les étudiants utilisent en moyenne **4 ressources numériques d’apprentissage par semaine**. | [https://www.ove-national.education.fr/enquete/enquete-conditions-de-vie/](https://www.ove-national.education.fr/enquete/enquete-conditions-de-vie/) |  
| Documents à comprendre      | **Études Ouest-France Étudiants (2022)**                               | Les étudiants en droit citent les **documents administratifs** comme un point d’incompréhension majeur. | [https://www.ouest-france.fr/education/](https://www.ouest-france.fr/education/) |

---

### Mehdi – Auto-entrepreneur

| Fonctionnalité                  | Source / Étude                                                            | Justification chiffrée                                                                 | URL                                              |
|----------------------------------|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|--------------------------------------------------|

| Questions sur statuts fiscaux    | **Forum auto-entrepreneurs + simulateurs BGE, Adie**                      | En période de déclaration ou seuil, les recherches explosent → **pic mensuel x2 à x3**. | [https://www.bge.asso.fr](https://www.bge.asso.fr/auto-entrepreneur/) |

---

### Sophie – Employée en PME

| Fonctionnalité                        | Source / Étude                                                              | Justification chiffrée                                                                 | URL                                              |
|---------------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| Analyse de documents                  | **Benchmark outils ERP (SAP, EBP, Sage PME)**                               | Tâches documentaires répétées **3 à 5 fois/semaine** dans la majorité des services.     | [https://www.sage.com/fr-fr/](https://www.sage.com/fr-fr/) |
| Génération de rapports                | **Gartner Finance Automation Survey (2023)**                                | 68 % des collaborateurs PME génèrent **2 à 3 rapports synthétiques** par semaine.       | [https://www.gartner.com/en/insights/finance-automation](https://www.gartner.com/en/insights/finance-automation) |

