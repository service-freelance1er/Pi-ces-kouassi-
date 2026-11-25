# Pièces Auto Kouassi — site statique

Projet prêt pour GitHub Pages. Le site fonctionne sans serveur ni base de données.

## Mise en ligne sur GitHub Pages
1. Décompressez le ZIP.
2. Envoyez tous les fichiers et dossiers du projet dans votre dépôt GitHub (à la racine).
3. Dans GitHub : **Settings → Pages**.
4. Choisissez **Deploy from a branch**, branche `main`, dossier `/ (root)`, puis **Save**.
5. Ouvrez l'adresse GitHub Pages affichée par GitHub.

## Le seul fichier à modifier : `produits.js`
Il contient les coordonnées de la boutique et le catalogue. Pour chaque produit, modifiez :
- `nom` : nom affiché
- `prix` : prix en FCFA (nombre, sans espaces)
- `photo` : URL d'une image ou chemin tel que `images/mon-image.jpg`
- `description` : description
- `categorie` : catégorie utilisée dans le filtre
- `stock` : quantité disponible

Exemple :
```js
{ id: "plaquette-frein", nom: "Plaquette de frein", prix: 15000, photo: "images/plaquette.jpg", description: "Jeu de plaquettes", categorie: "Freinage", stock: 10 }
```
Gardez un `id` unique pour chaque produit.

## Tableau de bord visuel
Ouvrez `gestion.html` après avoir publié le site. Modifiez les champs puis cliquez sur **Télécharger produits.js**. Remplacez ensuite le fichier `produits.js` du dépôt GitHub par celui téléchargé.

## Pages
- `index.html` : accueil
- `boutique.html` : catalogue, recherche, catégories et tri par prix
- `produit.html` : fiche produit
- `panier.html` : panier sauvegardé dans le navigateur (localStorage)
- `commande.html` : formulaire qui prépare une commande WhatsApp
- `apropos.html` : présentation
- `contact.html` : coordonnées
- `gestion.html` : tableau de bord visuel

## À savoir
- Les commandes sont envoyées via WhatsApp : aucun paiement en ligne ni traitement serveur.
- Le stock affiché est informatif ; il n'est pas automatiquement décrémenté.
- Les images de démonstration utilisent des liens d'images en ligne. Vous pouvez les remplacer par vos propres photos.
- Le panier est stocké sur l'appareil du visiteur.
