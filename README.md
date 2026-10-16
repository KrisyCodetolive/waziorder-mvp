# WaziOrder — prototype SaaS de commandes

WaziOrder est un prototype frontend React + TypeScript pour aider les petits commerçants ivoiriens à gérer leur catalogue, leurs commandes, leurs clients et leurs livraisons.

## Fonctionnalités présentes

- Tableau de bord et indicateurs calculés depuis les données du prototype.
- Catalogue : ajouter un produit, rechercher et filtrer, activer/masquer un produit.
- Commandes : création manuelle, recherche, filtres et changement de statut.
- Clients : liste dérivée des commandes enregistrées.
- Livraisons : suivi des commandes actives et changement de statut.
- Vitrine : aperçu de boutique personnalisable et bouton de contact WhatsApp.
- Partage du lien (prototype) et message WhatsApp prérempli depuis une commande.
- Statistiques et paramètres.
- Interface responsive, navigation mobile et notifications toast.
- Persistance locale via `localStorage`.

## Lancer le projet

Prérequis : Node.js 20+ et npm.

```bash
npm install
npm run dev
```

Vite affiche une URL locale, généralement `http://localhost:5173`.

Pour compiler :

```bash
npm run build
npm run preview
```

## Important : limites de cette version

Cette livraison est un **prototype frontend**. Elle ne comprend pas encore de backend, de compte utilisateur réel, de synchronisation entre appareils, ni de base Supabase. Les données sont enregistrées dans le navigateur via `localStorage` et peuvent être perdues si le stockage du navigateur est effacé. N'utilise pas cette version seule pour traiter des données réelles ou sensibles de clients.

Le bouton de partage copie une URL d'exemple, mais aucune route publique dynamique ni aucun hébergement de boutique n'est encore configuré. Les produits utilisent des émojis en guise d'illustrations provisoires. Les paiements sont saisis manuellement et ne déclenchent aucun transfert d'argent.

## Prochaines étapes conseillées

1. Connecter Supabase Auth et PostgreSQL.
2. Ajouter les migrations et politiques RLS pour l'isolation de chaque boutique.
3. Brancher le catalogue et les commandes sur la base de données.
4. Construire une vraie route publique `/boutique/:slug` avec commande client.
5. Ajouter tests, gestion d'erreurs, protections anti-double soumission et vérifications serveur.
6. Ajouter les vrais flux de paiement uniquement après validation des exigences du fournisseur et du cadre réglementaire.
# waziorder-mvp
