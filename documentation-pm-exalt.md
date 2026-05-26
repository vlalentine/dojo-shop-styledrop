# Documentation PM — Boutique eXalt
> Produit le 26/05/2026 — Session de découverte produit

---

## 1. Parcours utilisateur complet

| # | Étape | Action utilisateur | Émotion | Point de friction potentiel |
|---|-------|-------------------|---------|----------------------------|
| 1 | **Découverte** | Arrive sur la homepage via lien partagé ou recherche | Curiosité, première impression | Pas de preuve sociale (avis, notes) — le site projette peu de confiance au premier coup d'œil |
| 2 | **Orientation** | Lit le hero banner, scanne les catégories (Vêtements, Accessoires, Papeterie, Limited Edition) | Exploration, intérêt | Pas de mise en avant de bestsellers ni de nouveautés — rien ne guide l'œil vers un premier produit |
| 3 | **Navigation catalogue** | Clique sur une catégorie ou va sur /shop, filtre les produits | Découverte | Les filtres et le tri existent mais l'absence d'indication stock en liste peut mener à une mauvaise surprise |
| 4 | **Découverte produit** | Clique sur une fiche produit | Intérêt, envie | — |
| 5 | **Évaluation produit** | Consulte l'image, la description, la taille, la couleur, le prix, la date de livraison estimée | Évaluation, hésitation | Une seule image par produit — pas de vue dos/détail. Pas d'avis clients. Guide des tailles absent |
| 6 | **Sélection options** | Choisit taille, couleur, quantité | Engagement | Si le produit est en rupture, l'indicateur est discret — l'utilisateur peut ne pas le voir avant d'ajouter au panier |
| 7 | **Ajout au panier** | Clique "Add to cart" | Satisfaction… ou frustration | Pas de retour visuel fort — l'utilisateur peut ne pas savoir si l'ajout a fonctionné |
| 8 | **Revue du panier** | Va sur /cart, vérifie les articles, quantités, total | Vérification | Le statut stock apparaît dans le panier — l'utilisateur découvre ici qu'un article est en rupture, trop tard |
| 9 | **Connexion / Inscription** | Doit se connecter avant de payer (redirection avec message d'erreur) | Friction, abandon potentiel | Le mur d'authentification arrive tardivement — l'utilisateur n'a pas été informé avant |
| 10 | **Saisie infos livraison** | Remplit nom, adresse, ville, pays, téléphone sur /checkout | Concentration, effort | Formulaire long sur une seule page — pas de barre de progression, pas de sauvegarde automatique |
| 11 | **Choix moyen de paiement** | Sélectionne carte / PayPal / virement, saisit les données | Attention, méfiance possible | Pas d'indicateur de sécurité visible (pas de cadenas, pas de mention sécurisé) |
| 12 | **Validation commande** | Clique sur le bouton de confirmation | Anticipation | Pas de récap complet avant validation définitive — risque d'erreur non détectée |
| 13 | **Confirmation** | Voit la page /order-confirmation | Soulagement, satisfaction | La page confirme mais ne donne pas de numéro de commande ni d'email de confirmation mentionné |
| 14 | **Suivi commande** | Va sur /order-history, trouve sa commande (statut : "Processing") | Attente, interrogation | Statut unique "Processing" — aucune mise à jour, pas de suivi livraison, pas d'ETD post-commande |
| 15 | **Livraison** | Reçoit le colis | Satisfaction (espérée) | Toute cette étape est hors app — aucun lien de tracking, aucune notification dans le profil |

---

## 2. Persona principal

**Le consultant eXalt**

- **Profil** : Consultant en mission, connaît la marque, commande pour lui-même (hoodie, tote bag, casquette)
- **Comportement** : Pressé, sait ce qu'il veut, ne browse pas — il vient avec un produit en tête
- **Canaux** : Souvent mobile, entre deux réunions
- **Frustrations principales** :
  - Redirection vers le login au moment de payer
  - Ressaisir ses informations à chaque commande
  - Pas de suivi post-achat sérieux
- **Ce qui compte pour lui** : Aller vite, avoir confiance que la commande est bien passée

---

## 3. User Stories

### Authentification
> En tant que consultant eXalt, je veux pouvoir me connecter avec mon email professionnel dès la homepage, afin de ne pas être bloqué au moment de payer.

> En tant que consultant eXalt, je veux rester connecté entre mes sessions, afin de ne pas ressaisir mes identifiants à chaque visite.

### Catalogue & recherche
> En tant que consultant eXalt, je veux rechercher un produit par nom directement depuis le catalogue, afin de trouver ce que je veux sans parcourir toutes les catégories.

> En tant que consultant eXalt, je veux voir si un produit est disponible dans ma taille avant de cliquer sur la fiche, afin de ne pas perdre de temps sur un article en rupture.

### Commande
> En tant que consultant eXalt, je veux valider ma commande en moins de 3 minutes, afin de pouvoir le faire entre deux réunions.

> En tant que consultant eXalt, je veux que mon adresse de livraison soit pré-remplie, afin de ne pas ressaisir mes informations à chaque commande.

### Suivi
> En tant que consultant eXalt, je veux recevoir une confirmation avec un numéro de commande, afin de savoir que ma commande a bien été enregistrée.

> En tant que consultant eXalt, je veux suivre le statut de ma livraison depuis mon profil, afin de savoir quand je vais recevoir mes articles.

---

## 4. Priorisation MoSCoW

| Priorité | User Story | Statut |
|----------|-----------|--------|
| **Must** | Se connecter avec son email pro dès la homepage | ✅ Prototypé |
| **Must** | Voir la disponibilité stock avant d'ouvrir la fiche | ✅ Prototypé |
| **Must** | Recevoir une confirmation avec numéro de commande | 🔲 À faire |
| **Should** | Rester connecté entre les sessions | 🔲 À faire |
| **Should** | Adresse pré-remplie à la deuxième commande | 🔲 À faire |
| **Should** | Suivre le statut de livraison depuis le profil | 🔲 À faire |
| **Could** | Rechercher un produit par nom depuis le catalogue | 🔲 À faire |
| **Won't** | Valider en moins de 3 minutes (KPI global) | — Résultat, pas une story |

---

## 5. Prototypes réalisés

### Feature 1 — Visibilité du stock
**Problème** : L'utilisateur découvrait la rupture de stock trop tard (dans le panier).

**Ce qui a été fait** :
- Badge "Rupture de stock" sur la carte produit dans le catalogue
- Carte en transparence pour les produits indisponibles
- Indicateur coloré (vert/rouge) sur la fiche produit
- Bouton "Indisponible" désactivé en remplacement de "Add to cart"

### Feature 2 — Connexion depuis la homepage
**Problème** : Le consultant devait chercher le lien de connexion dans le menu, et se retrouvait bloqué au checkout.

**Ce qui a été fait** :
- Bouton "Se connecter" visible directement sur le hero banner
- Si l'utilisateur est déjà connecté, le bouton devient "Mon compte"
