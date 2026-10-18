# Ma Boutique

Application de boutique en ligne construite avec **React**, étape par étape, dans le cadre de mon apprentissage du développement fullstack JavaScript. Chaque fonctionnalité prolonge la précédente : un seul projet, un seul dépôt, 8 étapes.

> Démo en ligne : _à compléter après le déploiement_

## Aperçu

_Ajoute ici une capture d'écran ou un GIF de l'application une fois l'exercice 8 terminé._

## Fonctionnalités

- Catalogue de produits récupéré depuis une API
- Ajout et suppression de produits
- Recherche en temps réel, filtres par catégorie et par stock, tri par prix
- Offre flash avec compte à rebours (-20 % sur les prix)
- Panier global : ajout, quantités, suppression, total
- Navigation multi-pages avec page de détail par produit et page 404
- Tunnel de commande en 3 étapes avec validation des champs
- Panier conservé après rechargement de la page (`localStorage`)
- Page de confirmation de commande

## Technologies

| Outil | Usage |
| --- | --- |
| React | Interface et composants |
| Vite | Outil de build et serveur de développement |
| React Router | Navigation entre les pages |
| Context API | État global (panier, produits) |
| [Fake Store API](https://fakestoreapi.com/products) | Source des produits |

## Installation

```bash
# 1. Cloner le dépôt
git clone <url-de-ton-depot>
cd ma-boutique

# 2. Installer les dépendances
npm install

# 3. Lancer le serveur de développement
npm run dev
```

L'application est alors disponible sur `http://localhost:5173`.

### Autres commandes

```bash
npm run build     # Génère la version de production
npm run preview   # Prévisualise la version de production
```

## Structure du projet

```
src/
├── components/   # Composants réutilisables (ProductCard, ProductList, Cart, FlashSale...)
├── pages/        # Une page par route (Home, Products, ProductDetail, Checkout, NotFound...)
├── context/      # Contexts (CartContext, ProductsContext)
├── hooks/        # Custom hooks (useProducts, useLocalStorage)
├── App.jsx       # Déclaration des routes
└── main.jsx      # Point d'entrée
```

_Adapte cet arbre à ta structure réelle._

## Parcours : 8 étapes

Chaque étape correspond à une branche Git (`exo-N-...`) fusionnée dans `main` et à un tag (`v1` à `v8`).

- [ ] **v1 - Catalogue** : ajouter et supprimer des produits (`useState`)
- [ ] **v2 - Filtres** : recherche, catégorie, stock, tri (événements)
- [ ] **v3 - Offre flash** : compte à rebours avec nettoyage (`useEffect`)
- [ ] **v4 - API** : produits récupérés par `fetch`, états chargement et erreur (`useEffect`)
- [ ] **v5 - Panier** : état global (Context API)
- [ ] **v6 - Pages** : navigation et détail produit (React Router)
- [ ] **v7 - Commande** : formulaire multi-étapes avec validation
- [ ] **v8 - Finalisation** : persistance, confirmation, README, déploiement

## Mes choix techniques

_Cette section est la plus importante. Réponds avec tes mots, à partir de ce que tu as vraiment décidé en codant._

### Où vit chaque état, et pourquoi ?

_Exemple de question à traiter : pourquoi les produits sont-ils dans un Context plutôt que dans les props ?_

### Comment les composants sont-ils découpés ?

_Pourquoi `ProductCard` est séparé de `ProductList` ? Qu'est-ce qui est réutilisable ?_

### Valeurs calculées et valeurs stockées

_Qu'as-tu calculé à chaque rendu plutôt que stocké dans un state (total du panier, liste filtrée...) ? Pourquoi ?_

### Gestion du chargement et des erreurs

_Comment l'application réagit-elle quand l'API est lente ou indisponible ?_

### Nettoyage des effets

_Que se passe-t-il quand on quitte la page pendant que le compte à rebours tourne ? Comment l'as-tu géré ?_

## Difficultés rencontrées

_Note ici les blocages réels et comment tu les as résolus. Un recruteur y verra ta façon de raisonner._

## Améliorations possibles

- Connexion réelle avec un back-end (Express + PostgreSQL)
- Enregistrement des commandes en base de données
- Pagination de la liste des produits
- Tests des composants

## Auteur

**Grâsty** - Étudiant en développement fullstack JavaScript