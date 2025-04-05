# Pertinence technique (technologies) ?

### Définitions

Un **ORM** (Object-Relational Mapping) est un type de programme informatique qui permet de simuler une base de données orientée objet à partir d’une base de données relationnelle.

---

### Langages

Nous utiliserons **TypeScript** pour développer notre frontend et backend. Nous allons profiter de sa gestion de types, son déploiement simple et de nombreux **ORM**. Nous allons aussi utilisé le runtime **Bun**, pour profitez de ses performances, sa gestion de dépendances et ses autres avantages.

Nous utiliserons **Python** pour développer notre pipeline **IA** et le **Backend IA**. Nous allons profiter de nombreuses librairies comme **LlamaIndex** et **LangChain**.

Nous allons utiliser **Biome** pour le formattage du code typescript. [Biome](https://biomejs.dev/) sera implémenté dans nos applications frontend et backend mais aussi dans notre IDE.

---

### Frameworks

Pour le frontend, nous utiliserons :

| framework | raisons |
| --- | --- |
| **NextJS** | - basé sur **React**
- supporté par **Bun**
- gestion de **routes** |
| Tailwindcss | une des **librairies css** les plus populaires |
| Shadcn-ui | librairie de **components ui** basé sur **tailwindcss** |
| Clerk | - permet l’oauth sur de nombreux providers
- fourni des **components ui** login, register … utilisant **shadcn-ui** |
| Tremor | librairie de **graphiques** basé sur **tailwindcss** |
| Stripe | - solution pour gérer les paiements en ligne.
- compatible **TypeScript** (via Stripe.js et Checkout)
- sécurisée et conforme aux normes **PCI DSS** (Payment Card Industry Data Security Standard) |
| Prisma ORM | - ORM simple et optimisé pour le typescript
- supporte supabase |
| UI | d’autres librairies ui basé sur tailwindcss comme
- magic ui
- aceternity ui |

Pour le backend, nous utiliserons :

| framework | raisons |
| --- | --- |
| **Hono** | - **web framework** simple d’utilisation
- supporté par **Bun**
- validation des routes via **zod**
- format des routes avec **OpenAPI**
- interface documentation routes avec **swagger-ui** |
| Prisma ORM | - ORM simple et optimisé pour le typescript
- supporte supabase |

---

### Outils

| outils | description |
| --- | --- |
| **Ollama** | gestion et lancements de modèles locals |
| **Groq** | api pour communiquer avec des modèles très performants |
| **Railway** | déploiement de nos ressources cloud (web apps, storage, database) |
| **Supabase** | - déploiement de database postgres (auth, vector & storage)
- permet le stockage et une gestion des users |
| **IDE** | VSCode, Cursor |
| Biome | formattage du code TypeScript pour le frontend et le backend |
| Tesseract.js | OCR open-source très avancé |

---

### Détails IA

| spécificité | détails |
| --- | --- |
| **modèle LLM** | llama3 8b / llama3 70b |
| **modèle Embeddings** | cf Supabase |
| **Vector Embeddings** | cf Supabase |
| **Format API** | OpenAPI |