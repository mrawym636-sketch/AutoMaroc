# 🚗 AutoMaroc

[![PHP](https://img.shields.io/badge/PHP-7.4%2B-blue)](https://www.php.net/)
[![MySQL](https://img.shields.io/badge/Database-MySQL%20%2F%20MariaDB-orange)](https://www.mysql.com/)
[![Responsive](https://img.shields.io/badge/Design-Responsive-purple)](#-fonctionnalités)
[![InfinityFree](https://img.shields.io/badge/Host-InfinityFree-purple)](https://infinityfree.com)
[![Gemini](https://img.shields.io/badge/AI-Google%20Gemini-blue)](https://ai.google.dev/)

**AutoMaroc** est une plateforme e-commerce dédiée à la vente de voitures d'occasion au Maroc.
Le projet comprend une boutique, un panier, une liste de souhaits, l'authentification des utilisateurs, les commandes, les avis clients, un chatbot IA et des outils de gestion complets.

---

## 🚀 Démo

- **Site client :** [http://automaroc.great-site.net/pages/home.php](http://automaroc.great-site.net/pages/home.php)
- **Espace admin :** [http://automaroc.great-site.net/admin/login.php](http://automaroc.great-site.net/admin/login.php)
  - **Email :** `admin@admin.com`
  - **Mot de passe :** `admin123`

> ⚠️ **Sécurité :** Ces identifiants sont fournis pour la démonstration. Changez-les avant tout déploiement en production.

---

## ✨ Fonctionnalités

- 📦 Catalogue de véhicules avec catégories et marques
- 🔍 Recherche et pages de détails véhicule
- 🛒 Panier avec ajout, modification des quantités et suppression
- ❤️ Liste de souhaits
- 👤 Inscription, connexion et profil utilisateur
- 📦 Passage de commande et historique des commandes
- ⭐ Avis et système de notation (étoiles)
- 📞 Formulaire de contact et newsletter
- 🤖 Chatbot d'assistance en français, arabe/darija et anglais
- 📱 Mise en page responsive
- 🛠️ Tableau de bord admin complet (véhicules, stocks, commandes, utilisateurs, avis, paramètres, analyses)

---

## 🛠️ Technologies

- **Backend :** PHP avec PDO
- **Base de données :** MySQL ou MariaDB
- **Frontend :** HTML, CSS et JavaScript
- **Interface :** CSS personnalisé responsive
- **Icônes et polices :** Font Awesome et Google Fonts
- **Graphiques :** Chart.js
- **Tableaux :** DataTables
- **Chatbot :** Google Gemini API

---

## 📁 Structure du projet

```text
automaroc/
├── assets/
│   ├── css/
│   ├── images/
│   ├── js/
│   └── uploads/
├── pages/                  # Pages de la boutique
│   ├── home.php
│   ├── products.php
│   ├── product-details.php
│   ├── cart.php
│   ├── checkout.php
│   ├── orders.php
│   ├── order-details.php
│   ├── wishlist.php
│   ├── profile.php
│   ├── login.php
│   ├── register.php
│   ├── about.php
│   ├── review.php
│   ├── contact.php
│   └── install.php
├── php_files/              # Configuration et traitements PHP
│   ├── config.php
│   ├── login.php
│   ├── register.php
│   ├── add_to_cart.php
│   ├── get_cart.php
│   ├── update_cart.php
│   ├── remove_cart.php
│   ├── checkout.php
│   ├── add_review.php
│   ├── get_reviews.php
│   ├── chatbot.php
│   └── contact.php
├── admin/                  # Espace administrateur
│   ├── index.php
│   ├── login.php
│   ├── auth.php
│   ├── config.php
│   ├── header.php
│   ├── footer.php
│   ├── products.php
│   ├── product-add.php
│   ├── product-edit.php
│   ├── categories.php
│   ├── brands.php
│   ├── orders.php
│   ├── order-details.php
│   ├── users.php
│   ├── crud_users.php
│   ├── reviews.php
│   ├── coupons.php
│   ├── newsletter.php
│   ├── analytics.php
│   ├── inventory.php
│   ├── logs.php
│   ├── pages.php
│   ├── settings.php
│   ├── blacklist.php
│   ├── export_orders.php
│   ├── export_products.php
│   ├── export_users.php
│   ├── export_reviews.php
│   ├── backup.php
│   ├── logout.php
│   └── create_admin.php
├── index.php
├── header.php
├── footer.php
├── auto maroc.sql              # Script de création de la base de données
├── README.md
└── ...
```

---

## ⚙️ Prérequis

- PHP 7.4 ou plus récent
- MySQL ou MariaDB
- Apache, Nginx ou un serveur PHP local (par exemple XAMPP)
- Extension PHP PDO MySQL
- Extension cURL (pour le chatbot)
- Extension GD si vous utilisez les fonctions de génération d'images

Composer n'est actuellement pas requis.

---

## 🚀 Installation locale

### 1. Cloner le projet

```bash
git clone https://github.com/mrawym636-sketch/automaroc.git
cd automaroc
```

### 2. Placer dans le dossier web

Avec XAMPP :

```text
C:/xampp/htdocs/automaroc
```

Avec un serveur Linux :

```text
/var/www/html/automaroc
```

### 3. Créer la base de données

```sql
CREATE DATABASE auto_maroc_db CHARACTER SET utf8 COLLATE utf8_general_ci;
```

Puis importer le fichier `khalid.sql` via phpMyAdmin ou en ligne de commande :

```bash
mysql -u root -p auto_maroc_db < khalid.sql
```

### 4. Configurer l'accès à MySQL

Modifier `php_files/config.php` :

```php
$host = 'localhost';
$dbname = 'auto_maroc_db';
$username = 'root';
$password = '';
```

### 5. Démarrer le site

Démarrer Apache et MySQL, puis ouvrir :

```text
http://localhost/automaroc/
```

---

## ☁️ Déploiement sur InfinityFree

### 1. Créer la base de données
Aller dans cPanel → MySQL Databases.

Créer une base (ex. `if0_43357943_automaroc`), créer un utilisateur et lui donner tous les privilèges.

### 2. Configurer `php_files/config.php`

```php
$host = 'sqlXXX.infinityfree.com';
$dbname = 'if0_43357943_automaroc';
$username = 'if0_43357943';
$password = 'VOTRE_MOT_DE_PASSE';
```

### 3. Importer la base de données
Aller dans phpMyAdmin d'InfinityFree, sélectionner la base et importer `khalid.sql`.

### 4. Téléverser les fichiers
Uploader le contenu du projet dans `htdocs/`.

Vérifier que `assets/uploads/` est accessible en écriture (755).

### 5. Accéder au site

```text
http://automaroc.great-site.net/pages/home.php
```

---

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

Voir `khalid.sql` à la racine du dépôt.

---

## 🔑 Compte administrateur

| Email | Mot de passe | Rôle |
| --- | --- | --- |
| `admin@admin.com` | `admin123` | `Admin` |

Créer un admin en SQL :

```sql
INSERT INTO utilisateurs (nom, email, password, role, photo) 
VALUES (
    'Administrateur',
    'admin@admin.com',
    '$2y$10$92IXUNpkjO0rOQ5byMi.Ye4oKoEa3Ro9llC/.og/at2.uheWG/igi',
    'admin',
    'default.png'
);
```

---

## 🎮 Utilisation

### Client

```text
http://localhost/automaroc/
http://automaroc.great-site.net/pages/home.php
```

### Admin

```text
http://localhost/automaroc/admin/login.php
http://automaroc.great-site.net/admin/login.php
```

| Page | URL |
| --- | --- |
| Dashboard | `admin/index.php` |
| Véhicules | `admin/products.php` |
| Commandes | `admin/orders.php` |
| Utilisateurs | `admin/users.php` |
| Avis | `admin/reviews.php` |
| Paramètres | `admin/settings.php` |
| Analyses | `admin/analytics.php` |

---

## 🔐 Sécurité

- Utilisez des mots de passe forts et uniques pour les comptes et la base de données.
- Changez les identifiants par défaut ou de démonstration avant le déploiement.
- Ne commitez ni secrets, ni sauvegardes contenant des données personnelles.
- Limitez l'accès aux scripts d'administration, d'installation, de diagnostic et de sauvegarde.
- Vérifiez les contrôles d'accès et la configuration du serveur avant toute mise en production.
- Protégez `php_files/.env` (clé API Gemini) via `.htaccess`.

---

## 🤝 Contribution

1. Forkez le dépôt.
2. Créez une branche : `git checkout -b feature/ma-fonctionnalite`.
3. Commitez vos changements.
4. Poussez votre branche et ouvrez une Pull Request.

---

## 📄 Licence

Aucun fichier de licence n'a été identifié dans le dépôt.
Contactez le propriétaire du projet pour connaître les conditions de réutilisation.

---

## 📬 Contact

- **Email :** `mrawym636@gmail.com`
- **WhatsApp :** `+212 723-699031`
- **Localisation :** Casablanca, Maroc
- **GitHub :** `@mrawym636-sketch`

Pour toute question, ouvrez une issue dans ce dépôt ou contactez le mainteneur via GitHub.

⭐ N'oubliez pas de laisser une étoile si ce projet vous plaît ! ⭐
