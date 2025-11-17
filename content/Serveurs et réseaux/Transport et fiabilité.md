# Fiche de Cours : Le Modèle Client-Serveur et Concepts Associés

Le **modèle Client-Serveur** est l'une des bases des réseaux informatiques modernes, assurant une communication organisée et hiérarchisée entre les utilisateurs et les serveurs. Il est composé de deux grands facteurs : les clients qui font les demandes et les serveurs qui y répondent.

---

## 1. Le Client et le Navigateur

Le **Client** (souvent le navigateur ou une application) est la partie qui envoie la requête.

### Rôle du Navigateur
Le plan est principalement axé sur le **navigateur**.
* Il retient les préférences de l'utilisateur, par exemple un thème sombre.
* Le **cache** permet de retenir certains sites.
* Le chargement est plus rapide lors d'une visite ultérieure (ex: les logos et images sont enregistrés dans le cache).

### Le Frontend
C'est la partie qui sera **visible par le client**.
* Il assure la communication entre le serveur et le client.
* Il permet d'assurer le bon fonctionnement de l'application/programme avec la conformité et la sécurité pour une bonne expérience utilisateur.
* Il génère des éléments **HTML** ou **CSS**, ou un code d'état (ex: 404).

---

## 2. Le Serveur et le Backend

Le **Serveur** est essentiellement un ordinateur qui va gérer, stocker, intégrer et diffuser des informations, des données ou des services au réseau informatique.

### Types de Serveurs
Il existe plusieurs types de serveurs :
* Serveurs de web.
* Serveurs de bases de données.
* Serveurs de messagerie.
* Serveurs de fichiers.

### Avantages du Serveur
* **Centralisation des données**.
* **Maintenance facilitée**.
* **Mutualisation des ressources** pour permettre une amélioration de la performance des entreprises et une amélioration de la productivité.
* La maintenance est simplifiée car le serveur peut être mis à jour sans impacter directement les clients.

### Le Backend
C'est la partie qui sera plus focalisée sur le **développement web** et qui sera côté logiciel serveur.
* Il contient la **logique du traitement des requêtes**.
* Il est conçu pour répondre à la demande des clients.
* Il gère la communication avec le Frontend.
* La logique est implémentée par différents langages, que ce soit Python, Java ou d'autres.
* Il gère la logique du traitement des requêtes, le contrôle des droits d'accès de l'utilisateur (**authentification et autorisation**), l'exécution de la **logique métier** (calculs, vérification, automatisation) et la préparation d'une requête à destination de la base de données pour obtenir ou modifier des informations.
* Le Backend et l'API agissent comme un **cerveau** qui comprend la demande du client et sait où la diriger pour qu'elle puisse ressortir une réponse.

---

## 3. Communication et Sécurité

### Sockets
Les **sockets** sont un peu l'intermédiaire entre le client et le serveur, permettant un **échange de données dans les deux sens**.
* Il faut le visualiser comme une sorte de **prise** où l'on se branche pour pouvoir accéder à ce qu'il y a derrière.
* Le socket est vu comme un point de terminaison.
* Une fois la connexion établie, le serveur utilise une **socket d'écoute** et le client une **socket de connexion**.
* La communication peut être fermée à la fin de l'échange.
* Les échanges se font sur les protocoles **TCP** et **IP** ou **UDP** (qui privilégie la rapidité). Si l'on veut se connecter à une application web, on passe par **HTTP** ou **HTTPS**.

### API (Application Programming Interface)
L'API est l'interface qui va permettre de **connecter plusieurs bases de données ou des programmes entre elles**.
* Son but est de leur permettre d'intégrer tout ce qu'elles vont récolter dans une architecture qui sera déjà établie.
* L'API sert d'intermédiaire entre le client et les ressources en termes du serveur.
* Protocoles d'API :
    * **REST** : Le plus courant, basé sur l'HTTP.
    * **SOAP** : Le plus ancien, basé sur l'HTML.
    * **GraphQL** : Récupère exactement les données souhaitées.
    * **gRPC** : Très rapide pour la communication entre services.
* Bonnes pratiques pour les API : documentation, sécurité, versionnage, code de réponse précis et optimisation.

### Sécurisation des Échanges
Le protocole **HTTPS** (HyperText Transfer Protocol Secure) a pour but de **sécuriser les échanges** sur le web entre le serveur et le client, via un chiffrement **SSL** et maintenant **TLS**. Il assure trois choses :
1.  L'**authentification** du serveur via un certificat numérique.
2.  Le **chiffrement des données** pour éviter les espions.
3.  L'**intégrité des données** (vérifier que les données n'ont pas été perdues durant le "voyage").

D'autres protocoles sécurisés existent :
* **SMTPS** (Simple Mail Transfer Protocol Secure) : Sécurisé via une négociation TLS.
* **SSH** (Secure Shell) : Utilisé pour les échanges à distance, il est de nature chiffrée.
* **FTPS** (File Transfer Protocol Secure) : Protocole de transfert de fichiers qui est aussi chiffré soit avec SSH, soit avec TLS.

---

## 4. Pool de Connexion (Connection Pool)

Un pool de connexion est un **mécanisme d'optimisation** qui maintient un ensemble de **connexions préétablies** entre l'application et la base de données.

### Fonctionnement
* Ce sont des connexions qui restent **ouvertes et disponibles à la demande**.
* Quand une application veut exécuter une requête SQL, elle **emprunte** une connexion dans le pool et la **restitue** au pool lorsque la requête est finie.
* Ceci évite la création et la suppression fréquente des connexions, opérations qui sont très coûteuses et qui peuvent ralentir le système pour les applications à fort trafic.
* Sans pool, chaque requête nécessiterait l'ouverture complète d'une connexion (créer un lien TCP, authentification, initialisation du protocole, exécution de la commande).
* Avec le pool, la connexion est établie une fois, et à chaque requête, on la récupère et on la réutilise.

### Avantages
* Réduit les coûts de création.
* **Gain de performance** et réduction du temps de latence.
* **Mutualisation** : les connexions peuvent être partagées.
* **Gestion de la charge** : limiter les connexions permet aussi de limiter la surcharge de la base de données.
* **Purge automatique** : si des connexions sont invalides ou non utilisées pendant un certain temps, elles sont supprimées.
* Améliore la vitesse, la stabilité et la **scalabilité** de l'application.

### Dimensions Pratiques
* **Taille minimale** : Définit un nombre de connexions qui restent toujours prêtes à être utilisées.
* **Taille maximale** : Permet d'empêcher la saturation et de limiter le nombre de connexions.
* **Durée de vie maximale** : Permet un renouvellement périodique pour supprimer les connexions inactives.
* **Temps d'attente maximale** : Définit combien de temps une requête attend pour une connexion.
* **Ajustement de la configuration** : Il faut ajuster la configuration en fonction du trafic, du matériel et des besoins réels de l'application.
    * Sous-estimer peut entraîner un blocage et augmenter les temps d'attente.
    * Surestimer peut dégrader les performances.

---

## 5. Le Cycle de l'Interaction Client-Serveur

1.  **Requête du Client** : Le client envoie une requête.
2.  **Socket** : La requête passe par un socket.
3.  **Backend et API** : Le serveur reçoit la requête au niveau du Backend. Le Backend utilise l'API pour exécuter la logique de traitement.
4.  **Pool de Connexion** : Le serveur utilise les pools de connexion pour interroger la base de données.
5.  **Traitement BDD** : Les données sont extraites ou modifiées selon la requête initiale.
6.  **Réponse au Client** : Après le traitement, la réponse est adaptée (données, page web complète, code d'état) et transmise aux clients vers le même socket qui a été utilisé de base.

Le modèle client-serveur est l'assurance d'une communication organisée et hiérarchisée entre les utilisateurs et les serveurs. Il permet une meilleure gestion des ressources, une centralisation des données et une maintenance simplifiée.
