# Return of Investment

## **Introduction**

Le Return on Investment (ROI) est un indicateur clé pour évaluer l'efficacité des investissements. Il mesure le rapport entre le bénéfice généré par notre projet ou une action et le coût initial engagé. En d'autres termes, le ROI permet de savoir si un investissement rapporte plus qu'il ne coûte, en exprimant ce résultat sous forme de pourcentage. Ce document présente une approche pratique pour calculer et optimiser le ROIs.

Avant toutes choses il est important de comprendre et de définir ce qui représente nos coût fixe qui sont défini dans la ressource [Buget](esp_docs/cahier_des_charges/pages/Budget.md) et la méthodologie de calcul de nos revenus nets. En effet sachat que notre application fait appel à des services externes payant qui sont facturer à l'utilisation, il est primordiale de connaitre et/ou estimer l'utilisation de chaque typologie d'utilisateur.   
 
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

Ici l'objectif est de définir le fonctionnement des éléments payants de l'application, et de comprendre les différentes utilisations issue de nos typologie d'utilisateur. Tout d'abbord ComptaCompanion permet de choisir un niveau de connaissance qui correspond au format de retour de l'ia plus ou moins détaille et complexe en fonction du niveau choisi ()

### **Niveaux de connaissances**

| cible | niveau de connaissance |
| --- | --- |
| particulier | beginner,   |
| autoentrepreneur | utilise l'application dans le cadre de ses activités professionelle (gestion, impôt, développement) | ingestion de documents, chat sur des documents et sur les connaissances de la plateforme, générations de rapports |
| PME |  utilise l'application dans le cadre de ses activités professionelle | chat sur les connaissances de la plateforme, chat sur les documents personel non soumis aux restrictions de l'entreprise, générations de rapports |

### **Questions prédéfinis**

Notre application comporte des niveaux de connaissances qui permettent d'adapter le contenu de la réponse en fonction du niveau de l'utilisateur sur le sujet, beginner, intermediate et pro ainsi que des questions prédéfinis en fonction de niveau chaque utilisateur.

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

### **Questions**

***Question Beginner :*** 

"Quelle est la différence entre actif et passif ?" → 48 caractères

"Comment calculer le seuil de rentabilité d’une entreprise ?" → 61 caractères

"Quels sont les ratios financiers les plus utilisés ?" → 50 caractères

"C’est quoi une écriture comptable d’amortissement ?" → 53 caractère

(48+61+50+53)/4 = 53 caractères par question en moyenne 

| Question | Taille estimée de la réponse |
|---|---|
| Actif vs Passif | 200 caractères |
| Seuil de rentabilité | 275 caractères |
| Ratios financiers | 225 caractères |
| Écriture d’amortissement | 250 caractères |

(200+275+225+250)/4 = 237 caractères par réponse en moyenne

***Question Intermediate :*** 

"Comment comptabiliser une variation de stock en fin d’exercice selon le PCG ?" → 84 caractères

"Quelle est la méthode de calcul du coût de revient en comptabilité analytique ?" → 84 caractères

"Comment interpréter un ratio d’endettement supérieur à 100 % dans une PME ?" → 91 caractères

"Dans quel compte enregistre-t-on une charge constatée d’avance en comptabilité ?" → 86 caractères

(84+84+91+86)/4 = 86 caractères par question en moyenne 

| Sujet | Taille estimée de la réponse |
|---|---|
| Variation de stock selon le PCG | ~300 caractères |
| Calcul du coût de revient | ~275 caractères |
| Ratio d’endettement > 100 % | ~300 caractères |
| Charge constatée d’avance | ~250 caractères |

(300+275+300+250)/4 = 281 caractères par réponse en moyenne 

***Question Pro :*** 

"Comment comptabiliser une cession d'immobilisation avec une plus-value selon les règles fiscales françaises ?"
-> 120 caractères

"Dans un rapprochement bancaire, comment traiter une écriture d’écart non justifiée datant de plus de 6 mois ?"
-> 125 caractères

"Quels sont les impacts comptables d’un crédit-bail sur le bilan et le compte de résultat selon les normes IFRS 16 ?"
-> 132 caractères

"Comment ventiler les charges indirectes dans une comptabilité analytique selon la méthode des centres d’analyse ?"
-> 122 caractères

(84+84+91+86)/4 = 124 caractères par question en moyenne 

| Sujet                                                                           | Taille estimée de la réponse |
|---------------------------------------------------------------------------------|------------------------------|
| Cession d'immobilisation avec plus-value (règles fiscales FR)                   | 450 caractères               |
| Traitement d’une écriture d’écart non justifiée dans un rapprochement bancaire  | 400 caractères               |
| Crédit-bail et impacts comptables selon IFRS 16                                 | 500 caractères               |
| Ventilation des charges indirectes par centre d’analyse (méthode analytique)    | 450 caractères               |
 

(400+450+500+400)/4 = 450 caractères par réponse en moyenne 

### **Ingéstion de documents**

| Profil utilisateur | Type de documents ingérables                                  | Taille estimée (caractères) | Nombre moyen de caractères | Nombre estimé de pages |
|--------------------|---------------------------------------------------------------|-----------------------------|----------------------------|------------------------|
| Beginner           | Fiches pédagogiques, Q&A simplifiées, glossaires              | 1 000 à 3 000               | 2 000                      | 1 à 1.5 pages          |
| Intermédiaire      | Articles de blog spécialisés, extraits de manuels, cas simples| 3 000 à 6 000               | 4 500                      | 2 à 3 pages            |
| Pro                | Normes (PCG, IFRS), rapports financiers, procédures internes  | 6 000 à 15 000+             | 10 500                     | 5 à 7 pages            |

### **Génération de rapports**

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

En supposant que la répartition des utilisateurs est uniforme nous avons 

| nombre total de caractères (questions)/mois | nombre total de caractères (réponses)/mois | nombre total de caractères (documents)/mois | nombre total de caactères (rapports)/mois |
|---------------------------------------------|--------------------------------------------|---------------------------------------------|-------------------------------------------|
| 713                                         | 968                                        | 17 000                                      | 9250                                      |

Une fois le nombre de caractère par fonctionnalités et par typologie estimé, il est important de réussir à comprendre la féquence d'utilisation pour nos trois persona.

| Typologie      | Questions posées/mois | Réponses générées/mois | Documents ingérés/mois | Rapports générés/mois |
|----------------|-----------------------|------------------------|------------------------|-----------------------|
| Beginner       | 80                    | 80                     | 2                      | 1.5                   |
| Intermédiaire  | 160                   | 160                    | 7.5                    | 6                     |
| Pro            | 300                   | 300                    | 22.5                   | 15                    |

En supposant que la répartition des utilisateurs est uniforme nous avons 

| nombre total de questions posées/mois | nombre total de réponses générées/mois | nombre total de documents ingérés/mois | nombre total de rapports générés/mois |
|---------------------------------------|----------------------------------------|----------------------------------------|---------------------------------------|
| 540                                   | 540                                    | 32                                     | 22.5                                  |

Nous avons donc en total de caratères utiliser par mois par services : 

| nombre total de caractères(questions)/mois | nombre total de réponses générées/mois | nombre total de documents ingérés/mois | nombre total de rapports générés/mois |
|--------------------------------------------|----------------------------------------|----------------------------------------|---------------------------------------|
| 385 020                                    | 522 720                                | 544 000                                | 208 125                               |

---

## **Revenu estimer**

On peux donc estimer via les rubriques précedantes les nombre d'utilisation est donc le nombre de caractère estimer utiliser par mois par typlologie de users.

par mois 

beginner | question/reponse : 46 400 | documents ingéré : 4 000 | rapport généré : 1 500 | total : 51900
intermediate | question/reponse : 58 720 | documents ingéré : 33 750 | rapport généré : 15 000 | total : 107 470
pro | question/reponse : 307 200 | documents ingéré : 236 250 | rapport généré : 90 000 | total : 633 450


---

## Retour sur investissement 

### Composantes clés

| Élément | Description | valeur |
| --- | --- | --- |
| Coûts initiaux | Dépenses totales | 
| Revenus | Chiffre d’affaires ou bénéfices directs générés. |
| Gain net | Revenus – Coûts (y compris coûts indirects). |

---

### Calcul

$$
\text{ROI} = \left( \frac{\text{Gain net}}{\text{Coût initial}} \right) \times 100 = \left( \frac{\text{Revenus} - \text{Coûts}}{\text{Coûts}} \right) \times 100
$$

$$
\text{ROI} = \left( \frac{\text{Gain net}}{\text{Coût initial}} \right) \times 100 = \left( \frac{\text{Revenus} - \text{Coûts}}{\text{Coûts}} \right) \times 100
$$

---

## Seuil de rentabilité

Pour déterminer le nombre d'unités nécessaires pour atteindre le seuil de rentabilité, on utilise la formule suivante :
$$
\text{Seuil} = \frac{\text{Charges fixes}}{\text{Prix de vente unitaire} - \text{Coût variable unitaire}}
$$
