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
- **Niveau technique/comptable** : Débutante avec un bon raisonnement analytique


### Persona 2 : Mehdi — L’Auto-entrepreneur

- **Âge** : 34 ans  
- **Statut** : Graphiste freelance, micro-entreprise  
- **Objectif** : Gérer efficacement sa compta sans y passer trop de temps, comprendre ses obligations  
- **Fréquence d’usage** : Régulière (1–2 fois/semaine)  
- **Fonctionnalités clés recherchées** :
  - Explication de lignes comptables / seuils URSSAF
  - Vérification rapide de factures ou statuts fiscaux
  - Génération de mini-rapports ou fiches de suivi
- **Niveau technique/comptable** : Intermédiaire


### Persona 3 : Sophie — La Collaboratrice PME Opérationnelle

- **Âge** : 42 ans  
- **Statut** : Assistante administrative dans une PME (25 pers.)  
- **Objectif** : Gagner du temps dans le traitement des documents et échanges avec l’expert-comptable  
- **Fréquence d’usage** : Quotidienne  
- **Fonctionnalités clés recherchées** :
  - Analyse de documents (bilan, factures, fiches de paie)
  - Génération de rapports synthétiques pour la direction
  - Automatisation des contrôles simples (TVA, échéances)
- **Niveau technique/comptable** : Opérationnelle avancée (mais pas experte)


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

## **Revenu estimer**

Ici il est primordiale de noter que les bénéfices de ComptaCompanion sont uniquement basés sur la marge faite par le'utilisations des fonctionalités 
Nous avons donc fixer des tarifications 100 fois suppérieur aux coût réel des réponses générés.

|Fonctionnalité|Cout réel (par 1M token)|Cout réel (par caractères)|Cout plateforme (par 1M token)|Cout plateforme (par caractères)|
|---|---|---|---|---|
|Questions|0.59$|14.75e-8$|59$|14.75e-6$|
|réponse|0.79$|19.75e-8$|79$|19.75e-6$|
|Ingestions de documents|0.10$|2.5e-8$|10$|2.5e-6$|
|Générations de rapports|0.79$|19.75e-8$|79$|19.75e-6$|

> Ici le coût de la génération de rapport est égale au coût d'une réponse, c'est à dire que l'on néglige les 1 à 10 phrases nécéssaire à la spécifications du contenu du rapport en comparaison des plusieurs page générées  

**Cout réel :**

Ce qui nous donne en multipliant le prix par l'utilisation estimer en nombre de caractères par fonctionnnalité par mois, le cout réel moyen d'un utilisateur par mois.


(14.75 × 10⁻⁸ × 42 840) + (19.75 × 10⁻⁸ × 58 140) + (2.5 × 10⁻⁸ × 62 337) + (19.75 × 10⁻⁸ × 23 130) = **0.0239 $**


**Cout plateforme :**

Ce qui nous donne en multipliant le prix par l'utilisation estimer en nombre de caractères par fonctionnnalité par mois, le cout réel d'un utilisateur par mois.

((14.75e-6$)x42 840)+((19.75e-6$)x58 140)+((2.5e-6$)x62 337)+((19.75e-6$)x23 130) = 2.39$

((14.75 × 10⁻⁶ $) × 42 840) + ((19.75 × 10⁻⁶ $) × 58 140) + ((2.5 × 10⁻⁶ $) × 62 337) + ((19.75 × 10⁻⁶ $) × 23 130) = **2.39 $**



**Revenus généré :**

On a donc par la différence entre notre coût réel et le cout de la plateforme les revenus moyen généré par un utilisateur par mois.

Revenus = 2.39$ - 0.0239$ = **2.3661$** = **2.08€**

> Ici le taux de convertion Dollar américain vers euro est de 0.88.

---

## Seuil de rentabilité

### Composantes clés

| Élément                      | Description                                                        | Valeur |
|------------------------------|--------------------------------------------------------------------|--------|
| Charges fixes                | Coûts fixes totaux (par exemple : loyers, salaires fixes)         |   36.39$ =  32.02€   |
| Prix de vente unitaire       | Prix de vente d'un produit ou service                              |  2.3661$ = 2.08€   |
| Coût variable unitaire       | Coût variable pour produire une unité (ex : matières premières)   | aucun     |

> Ici le taux de convertion Dollar américain vers euro est de 0.88.

> Dans notre cas de figure nous excluons de potentiel salaire ou frais de location du bureau ici l'objectif est de comprendre le nombre de clients nécéssaire pour atteindre un seuil de rentabilité par rapport à nos frais de matériel (server et services)

### Calcul

Pour déterminer le nombre de client nécessaires pour atteindre le seuil de rentabilité, on utilise la formule suivante :

$$
\text{Seuil} = \frac{\text{Charges fixes}}{\text{Prix de vente unitaire} - \text{Coût variable unitaire}}
$$

$$
\text{Seuil} = \left( \frac{2.3661}{36.39} \right) = 6,50\%
$$

---

## Retour sur investissement 

### Composantes clés

| Élément | Description | valeur |
| --- | --- | --- |
| Coûts initiaux | Dépenses totales | 36.39$ |
| Revenus | Chiffre d’affaires ou bénéfices directs générés. | 2.39$ |
| Gain net | Revenus – Coûts (y compris coûts indirects). |

---

### Calcul

$$
\text{ROI} = \left( \frac{\text{Gain net}}{\text{Coût initial}} \right) \times 100 = \left( \frac{\text{Revenus} - \text{Coûts}}{\text{Coûts}} \right) \times 100
$$

$$
\text{ROI} = \left( \frac{2.3661}{36.39} \right) \times 100 = 6,50\%
$$

---