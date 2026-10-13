# Luso — site de l'agence

Site de l'agence Luso, création de sites web et d'applications : services, démos, méthode, formules, FAQ et formulaire de devis.

Site statique (HTML, CSS, JavaScript), sans cookie ni service tiers : les polices sont hébergées dans `assets/fonts/`.

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

## Mise en ligne avec GitHub Pages

Dans le dépôt : **Settings → Pages → Build and deployment**, choisir **Deploy from a branch**, branche `main`, dossier `/ (root)`, puis **Save**. Le site est ensuite disponible à l'adresse `https://youcefml-byte.github.io/luso/`.

## Formulaire de contact

- Sur un hébergement **avec PHP** (o2switch, OVHcloud, Hostinger…), `contact.php` envoie chaque demande par email à l'adresse définie dans `RECIPIENT`.
- Sur **GitHub Pages** (pas de PHP), le formulaire ouvre la messagerie du visiteur avec un email pré-rempli à destination de l'adresse `CONTACT_EMAIL` définie dans le script de `index.html`.

## À compléter avant d'ouvrir l'agence

Les informations légales manquantes sont surlignées dans les pages (classe `todo`) : identité de l'entreprise, SIREN, adresse, directeur de la publication, médiateur de la consommation, prestataires.
