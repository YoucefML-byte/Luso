# Luso — site de l'agence

Site de l'agence Luso, création de sites web et d'applications : réalisations, méthode, offres, FAQ et formulaire de devis. Page unique, pensée d'abord pour le mobile, avec un bouton de devis collant en bas d'écran sur téléphone.

Site statique (HTML, CSS, JavaScript), sans cookie ni traceur : les polices sont hébergées dans `assets/fonts/`.

## Contenu

| Fichier | Rôle |
| --- | --- |
| `index.html` | Page d'accueil |
| `demos/citrine-site.html` | Démo restaurant : carte en photos, galerie, chef, avis, horaires en direct, réservation |
| `demos/citrine-app.html` | Démo d'application mobile de commande à emporter (même restaurant) |
| `demos/ebene-boutique.html` | Démo boutique en ligne d'un torréfacteur : catalogue filtrable, fiche produit, panier, paiement simulé |
| `demos/copeau-menuiserie.html` | Démo artisan menuisier : réalisations, croquis/réalisation, zone d'intervention, devis en étapes |
| `demos/ondine-coiffure.html` | Démo salon de coiffure : tarifs, équipe, galerie, prise de rendez-vous avec export agenda |
| `demos/img/` | Photos des démos (Unsplash, licence Unsplash) et sachets Ébène générés pour la démo |
| `mentions-legales.html` | Mentions légales (LCEN) |
| `confidentialite.html` | Politique de confidentialité (RGPD) |
| `contact.php` | Envoi des demandes de devis par email (hébergement PHP uniquement) |
| `assets/styles.css` | Styles communs |
| `assets/img/` | Captures des démos affichées dans la section Réalisations de l'accueil (à régénérer si les démos changent) |
| `assets/img/hero/` | 20 photos Unsplash (licence Unsplash) du héros animé, en WebP 216 × 306 |
| `assets/data/world-110m.json` | Tracés des pays pour le globe de la section contact (Natural Earth via world-atlas 2.0.2, arcs TopoJSON quantifiés) |
| `404.html` | Page d'erreur aux couleurs du site, servie par GitHub Pages pour toute adresse inconnue |
| `sitemap.xml`, `robots.txt` | Plan du site pour Google ; `robots.txt` n'est lu qu'à la racine d'un nom de domaine |
| `apple-touch-icon.png`, `assets/img/og.jpg` | Icône d'écran d'accueil iPhone et image d'aperçu des partages (1200 × 630) |

## Mise en ligne avec GitHub Pages

Dans le dépôt : **Settings → Pages → Build and deployment**, choisir **Deploy from a branch**, branche `main`, dossier `/ (root)`, puis **Save**. Le site est ensuite disponible à l'adresse `https://youcefml-byte.github.io/Luso/`.

## Formulaire de contact

- Sur un hébergement **avec PHP** (o2switch, OVHcloud, Hostinger…), `contact.php` envoie chaque demande par email à l'adresse définie dans `RECIPIENT`.
- Sur **GitHub Pages** (pas de PHP), les demandes sont envoyées par [Web3Forms](https://web3forms.com) grâce à la clé `WEB3FORMS_KEY` définie dans le script de `index.html` ; elles arrivent par email à l'adresse liée à cette clé. Si Web3Forms ne répond pas, le formulaire ouvre la messagerie du visiteur avec un email pré-rempli à destination de `CONTACT_EMAIL`.
- Si `WEB3FORMS_KEY` est vide, le formulaire passe par `contact.php`.

## À compléter avant d'ouvrir l'agence

Les informations légales manquantes sont surlignées dans les pages (classe `todo`) : identité de l'entreprise, SIREN, adresse, directeur de la publication, médiateur de la consommation, prestataires.

## Mise à jour des styles

GitHub Pages laisse les navigateurs garder `assets/styles.css` en cache pendant 10 minutes. Après chaque modification de ce fichier, changez le numéro `?v=` du lien `styles.css` dans `index.html`, `mentions-legales.html` et `confidentialite.html`, sinon un visiteur peut recevoir la nouvelle page avec l'ancienne feuille de style.

## Passer à un nom de domaine (ex. luso.fr)

1. Dans **Settings → Pages → Custom domain**, saisir le domaine, puis cocher **Enforce HTTPS** une fois le certificat prêt.
2. Remplacer `https://youcefml-byte.github.io/Luso/` par la nouvelle adresse dans :
   - `index.html` : balises `canonical`, `og:url`, `og:image` et données structurées (`application/ld+json`) ;
   - `mentions-legales.html` et `confidentialite.html` : balise `canonical` ;
   - `sitemap.xml` et `robots.txt`.
3. Déclarer le site et le `sitemap.xml` dans [Google Search Console](https://search.google.com/search-console).
