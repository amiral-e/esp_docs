# Pertinence technique (technologies) ?

### Définitions

Un **ORM** (Object-Relational Mapping) est un type de programme informatique qui permet de simuler une base de données orientée objet à partir d’une base de données relationnelle.

---

### Langages

Nous utiliserons **TypeScript** pour développer notre frontend et backend. Nous allons profiter de sa gestion de types, son déploiement simple et de nombreux **ORM**. Nous allons aussi utilisé le runtime **Bun**, pour profitez de ses performances, sa gestion de dépendances et ses autres avantages.

> Nous n'utilisons plus d'ORM mais le client supabase-js.

Nous utiliserons **Python** pour développer notre pipeline **IA** et le **Backend IA**. Nous allons profiter de nombreuses librairies comme **LlamaIndex** et **LangChain**.

> Après délibération et de une mise à jour de la version TypeScript de LlamaIndex, nous avons décidé de réimplémenter la logique du backend ia dans le backend principal.

Nous allons utiliser **Biome** pour le formattage du code typescript. [Biome](https://biomejs.dev/) sera implémenté dans nos applications frontend et backend mais aussi dans notre IDE.

---

### Frameworks & Outils

Pour le frontend, nous utiliserons :

| framework | raisons |
| --- | --- |
| NextJS | basé sur **React**, supporté par **Bun**
| Tailwindcss | une des **librairies css** les plus populaires
| Shadcn-ui | librairie de **components ui** basé sur **tailwindcss**
| Tremor | librairie de **graphiques** basé sur **tailwindcss**
| Stripe | gestion paiements en ligne, compatible **TypeScript** (Stripe.js et Checkout), sécurisé et conforme aux normes **PCI DSS** (Payment Card Industry Data Security Standard)
| UI | magic ui, aceternity ui...

Pour le backend, nous utiliserons :

| framework | raisons |
| --- | --- |
| Hono | **web framework** simple d’utilisation et léger, supporté par **Bun**, format des routes avec **OpenAPI**, documentation routes avec **scalar-ui**


Pour la base de données, nous utiliserons Supabase :

| outil | raisons |
| --- | --- |
| Supabase | bases de données postgres, authentification et gestion des users, envoie d'emails connection, inscriptions, vector stores
| Stripe | gestion des paiments 

---

### Outils

| outils | description |
| --- | --- |
| **Groq** | api pour communiquer avec des modèles performants
| **OpenAI** | utilisation d'un modèles pour généré et questionner les embeddings des documents
| **Fly.io** | déploiement de nos ressources cloud (web apps)
| **IDE** | VSCode, Cursor
| Biome | formattage du code TypeScript pour le frontend et le backend

---

### Détails IA

| spécificité | détails |
| --- | --- |
| **modèle LLM** | llama3.3 70b Versatille 128k context
| **modèle Embeddings** | ada 002
| **Vector Embeddings** | Supabase
| **Format API** | OpenAPI

> Nous avons choisis d'utiliser un modèle récent (llama 3.3 6 décembre 2024), avec un temps de réponse rapide (275 token par seconde) et la plus grosse taille de context (128k tokens en input).

> Nous avons utilisé le modèle d'embeddings ada 002 d'OpenAI. Lors de la mise en place du projet c'était le modèle recommandé et le plus courrant. Nous pourrions passer sur le dernier modèle 3-small pour réduire les couts.