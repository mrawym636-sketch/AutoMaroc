# 🚗 AutoMaroc

[![PHP](https://img.shields.io/badge/PHP-7.4%2B-blue)](https://www.php.net/)
[![MySQL](https://img.shields.io/badge/Database-MySQL%20%2F%20MariaDB-orange)](https://www.mysql.com/)
[![Responsive](https://img.shields.io/badge/Design-Responsive-purple)](#-fonctionnalités)
[![InfinityFree](https://img.shields.io/badge/Host-InfinityFree-purple)](https://infinityfree.com)
[![Gemini](https://img.shields.io/badge/AI-Google%20Gemini-blue)](https://ai.google.dev/)

**AutoMaroc** est une plateforme e-commerce dédiée à la vente de voitures d'occasion au Maroc. Le projet comprend une boutique, un panier, une liste de souhaits, l'authentification des utilisateurs, les commandes, les avis clients, un chatbot IA et des outils de gestion.

## 🚀 Démo

- **Site client :** [automaroc.great-site.net](http://automaroc.great-site.net/pages/home.php)
- **Espace administrateur :** [Connexion](http://automaroc.great-site.net/admin/login.php)

> ⚠️ Les identifiants de démonstration ne sont pas publiés dans ce dépôt. Ne déployez jamais de compte administrateur avec un mot de passe par défaut ou partagé. Utilisez des identifiants forts et uniques.

## ✨ Fonctionnalités

- 📦 Catalogue de véhicules avec catégories et marques
- 🔍 Recherche et pages de détails des véhicules
- 🛒 Panier avec ajout, modification des quantités et suppression
- ❤️ Liste de souhaits
- 👤 Inscription, connexion et profil utilisateur
- 📦 Passage de commande et historique des commandes
- ⭐ Avis et système de notation
- 📞 Formulaire de contact et newsletter
- 🤖 Chatbot d'assistance en français, arabe/darija et anglais
- 📱 Mise en page responsive
- 🛠️ Tableau de bord administrateur : véhicules, stocks, commandes, utilisateurs, avis, paramètres et analyses

## 🛠️ Technologies

- **Backend :** PHP avec PDO
- **Base de données :** MySQL ou MariaDB
- **Frontend :** HTML, CSS et JavaScript
- **Icônes et polices :** Font Awesome et Google Fonts
- **Graphiques :** Chart.js
- **Tableaux :** DataTables
- **Chatbot :** Google Gemini API

## 📁 Structure du projet

```text
automaroc/
├── assets/
│   ├── css/
│   ├── images/
│   ├── js/
│   └── uploads/
├── pages/                  # Pages de la boutique
├── php_files/              # Configuration et traitements PHP
├── admin/                  # Espace administrateur
├── index.php
├── header.php
├── footer.php
├── khalid.sql              # Script de création de la base de données
└── README.md
```

Les pages et traitements PHP incluent notamment le catalogue, les détails d'un véhicule, le panier, le paiement, les commandes, le profil, l'authentification, les avis et le chatbot. L'espace d'administration permet la gestion du catalogue, des commandes, des utilisateurs et des paramètres.

## ⚙️ Prérequis

- PHP 7.4 ou plus récent
- MySQL ou MariaDB
- Apache, Nginx ou un serveur PHP local (par exemple XAMPP)
- Extension PHP PDO MySQL
- Extension cURL pour le chatbot
- Extension GD si vous utilisez les fonctions de génération d'images

Composer n'est actuellement pas requis.

## 🚀 Installation locale

### 1. Cloner le projet

```bash
git clone https://github.com/mrawym636-sketch/automaroc.git
cd automaroc
```

### 2. Placer le projet dans le dossier web

Avec XAMPP :

```text
C:/xampp/htdocs/automaroc
```

Avec un serveur Linux :

```text
/var/www/html/automaroc
```

### 3. Créer et importer la base de données

Créer la base de données :

```sql
CREATE DATABASE auto_maroc_db CHARACTER SET utf8 COLLATE utf8_general_ci;
```

Importer ensuite `khalid.sql` avec phpMyAdmin ou en ligne de commande :

```bash
mysql -u root -p auto_maroc_db < khalid.sql
```

### 4. Configurer l'accès à MySQL

Dans `php_files/config.php`, renseigner les paramètres locaux de la base :

```php
$host = 'localhost';
$dbname = 'auto_maroc_db';
$username = 'root';
$password = '';
```

Adaptez ces valeurs à votre environnement. Ne commitez pas de mots de passe ni de clés API.

### 5. Démarrer le site

Démarrer Apache et MySQL, puis ouvrir :

```text
http://localhost/automaroc/
```

## ☁️ Déploiement sur InfinityFree

1. Dans le cPanel, créer une base de données et un utilisateur, puis attribuer à celui-ci les privilèges requis.
2. Configurer les paramètres de connexion dans `php_files/config.php` avec les informations fournies par l'hébergeur.
3. Importer `khalid.sql` dans la base via phpMyAdmin.
4. Téléverser les fichiers du projet dans `htdocs/` et vérifier les permissions nécessaires pour `assets/uploads/`.
5. Configurer les secrets, notamment la clé API Gemini, hors du contrôle de version.
6. Accéder au site depuis son domaine.

> Les noms d'hôtes, identifiants et paramètres de base de données varient selon le compte d'hébergement. Consultez le panneau de contrôle de l'hébergeur plutôt que de reprendre des exemples d'identifiants.

## 🗄️ Base de données

Le code utilise notamment les tables suivantes :

| Table | Description |
| --- | --- |
| `utilisateurs` | Comptes utilisateurs |
| `produits` | Catalogue de véhicules |
| `categories` | Catégories de véhicules |
| `brands` | Marques |
| `commandes` | Commandes clients |
| `commande_logs` | Historique des changements de statut |
| `avis` | Avis et notes |
| `messages` | Messages de contact |
| `newsletter_subscribers` | Abonnements à la newsletter |
| `chat_logs` | Historique du chatbot |
| `pages` | Contenu des pages |
| `logs` | Journal d'activité |
| `blacklist` | Numéros bloqués |
| `coupons` | Codes promo |
| `settings` | Paramètres généraux |

Le script de création de la base de données se trouve dans [`khalid.sql`](khalid.sql).

## 🎮 Utilisation

En local :

```text
Boutique : http://localhost/automaroc/
Administration : http://localhost/automaroc/admin/login.php
```

Pages d'administration principales :

| Page | URL relative |
| --- | --- |
| Dashboard | `admin/index.php` |
| Véhicules | `admin/products.php` |
| Commandes | `admin/orders.php` |
| Utilisateurs | `admin/users.php` |
| Avis | `admin/reviews.php` |
| Paramètres | `admin/settings.php` |
| Analyses | `admin/analytics.php` |

## 🔐 Sécurité

- Utilisez des mots de passe forts et uniques pour les comptes et la base de données.
- Changez tout identifiant par défaut ou de démonstration avant le déploiement.
- Ne commitez ni secrets, ni clés API, ni sauvegardes contenant des données personnelles.
- Limitez l'accès aux scripts d'administration, d'installation, de diagnostic et de sauvegarde.
- Vérifiez les contrôles d'accès et la configuration du serveur avant toute mise en production.
- Protégez les fichiers de configuration et secrets (notamment la clé API Gemini) contre tout accès web direct.
- Utilisez HTTPS pour le site déployé.

## 🤝 Contribution

1. Forkez le dépôt.
2. Créez une branche : `git checkout -b feature/ma-fonctionnalite`.
3. Commitez vos changements.
4. Poussez votre branche et ouvrez une Pull Request.

## 📄 Licence

Aucun fichier de licence n'a été identifié dans le dépôt. Contactez le propriétaire du projet pour connaître les conditions de réutilisation.

## 📬 Contact

- **Email :** mrawym636@gmail.com
- **WhatsApp :** +212 723-699031
- **Localisation :** Casablanca, Maroc
- **GitHub :** [@mrawym636-sketch](https://github.com/mrawym636-sketch)

Pour toute question, ouvrez une issue dans ce dépôt ou contactez le mainteneur via GitHub.

⭐ N'oubliez pas de laisser une étoile si ce projet vous plaît ! ⭐
