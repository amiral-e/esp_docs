# Return of Investment

### **Introduction**

Le Return on Investment (ROI) est un indicateur clé pour évaluer l'efficacité des investissements. Il mesure le rapport entre le bénéfice généré par notre projet ou une action et le coût initial engagé. En d'autres termes, le ROI permet de savoir si un investissement rapporte plus qu'il ne coûte, en exprimant ce résultat sous forme de pourcentage. Ce document présente une approche pratique pour calculer et optimiser le ROIs.

---

### Etude de marché

**Nos concurrents :** 

| plateform | fonctionnalité | offre (prix/mois)|
| --- | --- | --- |
| Humata | Ingestion et chat sur des documents | Expert 9.99 $ |
| Juribot | ChatIA (entrainer sur du droit) | offre personnalisée sur demande |
| sinao | Devis, Suivi des paiements, Facturation électronique, Déclaration et paiement TVA, Suivi financier | 11,40 € |
| LegiGPT | ChatIA (entrainer sur du droit)  | offre personnalisée sur demande |

**Nos clients cibles et leurs besoins :** 

| cible | description | besoins |
| --- | --- | --- |
| particulier | utilise l'application dans le cadre de recherches personelles  | ingestion de documents, chat sur des documents et sur les connaissances de la plateforme, générations de rapports |
| autoentrepreneur | utilise l'application dans le cadre de ses activités professionelle (gestion, impôt, développement) | ingestion de documents, chat sur des documents et sur les connaissances de la plateforme, générations de rapports |
| PME |  utilise l'application dans le cadre de ses activités professionelle | chat sur les connaissances de la plateforme, chat sur les documents personel non soumis aux restrictions de l'entreprise, générations de rapports |

**Estimation des intéractions par utilisateur cible :** 

Interactions communes : 
- chat sur les connaissances de la plateforme

Particulier : 
- ingestion de documents 
    - cours de droit et finance
    - sujet d'examen
    - documents tiers
- chat sur les documents personel
- générations de rapports
    - fiche de cours
    - note personelle 

Autoentrepreneur : 
- ingestion de documents 
    - devis
    - fiche d'impot 
    - document de l'ursaf
    - documents tiers 
- chat sur les documents personel
- générations de rapports
    - rapport annuelle sur l'activité
    - rapport de l'évolution d'année en année
    - notes personelle 

PME : 
- ingestion de documents 
    - soumis aux restrictions de l'entreprise
- chat sur les documents
- générations de rapports
    - notes personelle 
    
---

## Utilisations

### Niveaux de connaissances

Notre application comporte des niveaux de connaissances qui permettent d'adapter le contenu de la réponse en fonction du niveau de l'utilisateur sur le sujet, beginner, intermidiaire et pro.


| cible | niveau de connaissance |
| --- | --- |
| particulier | beginner,   |
| autoentrepreneur | utilise l'application dans le cadre de ses activités professionelle (gestion, impôt, développement) | ingestion de documents, chat sur des documents et sur les connaissances de la plateforme, générations de rapports |
| PME |  utilise l'application dans le cadre de ses activités professionelle | chat sur les connaissances de la plateforme, chat sur les documents personel non soumis aux restrictions de l'entreprise, générations de rapports |

### Questions prédéfinis

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

## Utilsation estimer par typologie d'utilisateur 

### Questions

***Question Beginner :*** 

"Quelle est la différence entre actif et passif ?" → 48 caractères

"Comment calculer le seuil de rentabilité d’une entreprise ?" → 61 caractères

"Quels sont les ratios financiers les plus utilisés ?" → 50 caractères

"C’est quoi une écriture comptable d’amortissement ?" → 53 caractère

(48+61+50+53)/4 = 53 caractères par question en moyenne 

| Question | Taille estimée de la réponse |
|---|---|
| Actif vs Passif | ~200 caractères |
| Seuil de rentabilité | ~275 caractères |
| Ratios financiers | ~225 caractères |
| Écriture d’amortissement | ~250 caractères |

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

### Ingéstion de documents

| Profil utilisateur | Type de documents ingérables                                  | Taille estimée (caractères) | Nombre moyen de caractères | Nombre estimé de pages |
|--------------------|---------------------------------------------------------------|-----------------------------|----------------------------|------------------------|
| Beginner           | Fiches pédagogiques, Q&A simplifiées, glossaires              | 1 000 à 3 000               | 2 000                      | 1 à 1.5 pages          |
| Intermédiaire      | Articles de blog spécialisés, extraits de manuels, cas simples| 3 000 à 6 000               | 4 500                      | 2 à 3 pages            |
| Pro                | Normes (PCG, IFRS), rapports financiers, procédures internes  | 6 000 à 15 000+             | 10 500                     | 5 à 7 pages            |

### Génération de rapports 

| Type de rapport généré                                    | Profil cible       | Taille estimée (caractères) | Taille moyenne estimée | Taille estimée (pages) |
|-----------------------------------------------------------|--------------------|-----------------------------|------------------------|------------------------|
| Résumé d’un document (synthèse simple)                    | Beginner           | 800 à 1 200                 | 1 000                  | 0.5 page               |
| Résumé explicatif ou reformulation pédagogique            | Intermédiaire      | 1 500 à 3 000               | 2 250                  | 1 à 1.5 pages          |
| Rapport d’analyse ou diagnostic comptable/financier       | Pro                | 3 000 à 6 000               | 4 500                  | 2 à 3 pages            |
| Rapport avec recommandations ou plan d’action             | Pro                | 5 000 à 10 000              | 7 500                  | 2.5 à 5 pages          |

### Utilisation estimer global par typologie d'utilisateur

| Profil utilisateur | Question/réponse (caractères) | ingestion de documents (caractères) | génération de rapport (caractères) |
|--------------------|-------------------------------|-------------------------------------|------------------------------------|
| Beginner           | 290                           | 2 000                               | 1 000                              |
| Intermédiaire      | 367                           | 4 500                               | 2 250                              |
| Pro                | 574                           | 10 500                              | 6 000                              |

---

## Revenu estimer

 Maintenant que l'on connais le nombre de caractère estimé moyen par action par typologie d'utilisateur, il nous faut déterminer la fréquence d'utilisation par typologie d'utilisateur.


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
