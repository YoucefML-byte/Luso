# Luso — site de l'agence

Site de l'agence Luso, création de sites web et d'applications : réalisations, méthode, offres, FAQ et formulaire de devis. Page unique, pensée d'abord pour le mobile, avec un bouton de devis collant en bas d'écran sur téléphone.

Site statique (HTML, CSS, JavaScript), sans cookie ni traceur : les polices sont hébergées dans `assets/fonts/`.

## Contenu

| Fichier | Rôle |
| --- | --- |
| `index.html` | Page d'accueil |
| `demos/citrine-site.html` | Démo de site vitrine (restaurant fictif) |
| `demos/citrine-app.html` | Démo d'application mobile de commande |
| `mentions-legales.html` | Mentions légales (LCEN) |
| `confidentialite.html` | Politique de confidentialité (RGPD) |
| `contact.php` | Envoi des demandes de devis par email (hébergement PHP uniquement) |
| `assets/styles.css` | Styles communs |
| `assets/img/` | Captures des démos Citrine affichées sur l'accueil (à régénérer si les démos changent) |
| `assets/img/hero/` | 20 photos Unsplash (licence Unsplash) du héros animé, en WebP 216 × 306 |

## Mise en ligne avec GitHub Pages

Dans le dépôt : **Settings → Pages → Build and deployment**, choisir **Deploy from a branch**, branche `main`, dossier `/ (root)`, puis **Save**. Le site est ensuite disponible à l'adresse `https://youcefml-byte.github.io/Luso/`.

## Formulaire de contact

- Sur un hébergement **avec PHP** (o2switch, OVHcloud, Hostinger…), `contact.php` envoie chaque demande par email à l'adresse définie dans `RECIPIENT`.
- Sur **GitHub Pages** (pas de PHP), les demandes sont envoyées par [Web3Forms](https://web3forms.com) grâce à la clé `WEB3FORMS_KEY` définie dans le script de `index.html` ; elles arrivent par email à l'adresse liée à cette clé. Si Web3Forms ne répond pas, le formulaire ouvre la messagerie du visiteur avec un email pré-rempli à destination de `CONTACT_EMAIL`.
- Si `WEB3FORMS_KEY` est vide, le formulaire passe par `contact.php`.

## À compléter avant d'ouvrir l'agence

Les informations légales manquantes sont surlignées dans les pages (classe `todo`) : identité de l'entreprise, SIREN, adresse, directeur de la publication, médiateur de la consommation, prestataires.
