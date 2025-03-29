Starzy - Plateforme de Réservation d'Événements et de Vente de Produits Astronomiques

Description du Projet

Starzy est une plateforme innovante qui permet aux utilisateurs de :

Réserver des événements d'astronomie en achetant des tickets en ligne.

Acheter des produits liés à l'astronomie via une boutique intégrée.

Participer à des rencontres collaboratives en temps réel.

Accéder à une bibliothèque de ressources incluant des livres, vidéos et articles de blog.

Laisser des commentaires sur les contenus et interagir avec la communauté.

Effectuer des paiements sécurisés pour leurs achats et réservations.

Fonctionnalités Principales

1. Gestion des Utilisateurs

Inscription et connexion sécurisées.

Gestion du profil utilisateur.

Historique des achats et réservations.

Participation aux rencontres collaboratives.

2. Réservation d'Événements

Consultation de la liste des événements disponibles.

Achat de tickets en ligne.

Gestion des réservations.

3. Boutique en Ligne

Consultation et achat de produits liés à l'astronomie.

Gestion des commandes et des paiements.

Classification des produits par catégories et marques.

4. Gestion des Contenus et Ressources

Accès à une bibliothèque de livres et vidéos.

Lecture et écriture d'articles de blog.

Système de commentaires pour chaque ressource.

5. Paiements Sécurisés

Paiement des commandes et des tickets via différentes méthodes (Carte bancaire, PayPal, etc.).

Gestion du statut des paiements (en attente, validé, échoué).

Modèle de Données

Entités et Relations

Utilisateur (User)

Attributs : user_id, name, email, password

Relations :

Peut acheter plusieurs tickets.

Peut participer à plusieurs rencontres.

Peut laisser plusieurs commentaires.

Peut effectuer plusieurs paiements.

Événement (Event)

Attributs : event_id, name, date_début, date_fin, location

Relations :

Possède plusieurs tickets.

Un utilisateur peut acheter plusieurs tickets pour différents événements.

Ticket

Attributs : ticket_id, price, event_id, user_id

Relations :

Lié à un événement et un utilisateur.

Produit (Product)

Attributs : product_id, name, price, description, category, image, marque, disponibilité, garantie

Relations :

Un utilisateur peut acheter plusieurs produits.

Rencontre (Meeting)

Attributs : meeting_id, name, date_début, date_fin

Relations :

Peut inclure plusieurs utilisateurs participants.

Livre (Book)

Attributs : book_id, title, author, genre, publication_date

Relations :

Un utilisateur peut laisser un commentaire.

Vidéo (Video)

Attributs : video_id, title, creator, genre, publication_date

Relations :

Un utilisateur peut laisser un commentaire.

Blog

Attributs : blog_id, title, content, author_id

Relations :

Un utilisateur peut écrire plusieurs blogs.

Commentaire (Comment)

Attributs : comment_id, user_id, content, date_commentaire

Relations :

Lié à un utilisateur et une ressource (livre, vidéo ou blog).

Commande (Order)

Attributs : id_commande, id_utilisateur, date_commande, total, statut, description, quantité, prix_unitaire

Relations :

Liée à un utilisateur via id_utilisateur.

Contient plusieurs produits via une table de jointure.

Paiement (Payment)

Attributs : payment_id, amount, payment_method, payment_status, user_id

Relations :

Un utilisateur peut effectuer plusieurs paiements.

Lié à une commande spécifique.

Technologies Utilisées

Back-end : PHP (Framework MVC)

Base de données : Oracle

Front-end : HTML, CSS, JavaScript

Sécurité : Authentification sécurisée, gestion des paiements

Installation et Déploiement

Cloner le dépôt :

git clone https://github.com/votre-repository/starzy.git

Configurer la base de données Oracle.

Modifier le fichier Config.php avec les informations de connexion.

Lancer le serveur local avec Apache et PHP.