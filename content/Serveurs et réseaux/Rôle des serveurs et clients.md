# Fiche de Cours : Le Modèle Client-Serveur et Concepts Associés

Le **modèle Client-Serveur** est l'une des bases des réseaux informatiques modernes, assurant une communication organisée et hiérarchisée entre les utilisateurs et les serveurs. Il est composé de deux grands facteurs : les clients qui font les demandes et les serveurs qui y répondent.

---

## 1. Le Client et le Navigateur

Le **Client** (souvent le navigateur ou une application) est la partie qui envoie la requête.

### Rôle du Navigateur
Le plan est principalement axé sur le **navigateur**, qui a pour but de rester dans le navigateur.
* Il retient les préférences de l'utilisateur (ex: thème sombre).
* Le **cache** permet de retenir certains sites et accélère le chargement lors d'une visite ultérieure (ex: les logos et images sont déjà enregistrés).

### Le Frontend
C'est la partie qui est **visible par le client**.
* Il assure la communication entre le serveur et le client.
* Il permet d'assurer le bon fonctionnement de l'application/programme, y compris la conformité et la sécurité pour une bonne expérience utilisateur.
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
* **Mutualisation des ressources** pour améliorer la performance et la productivité des entreprises.
* La maintenance peut être simplifiée car le serveur peut être mis à jour sans impacter directement les clients.

### Le Backend
C'est la partie qui sera plus focalisée sur le **développement web** et se situe côté logiciel serveur.
* Il contient la **logique du traitement des requêtes**, souvent implémentée par différents langages (Python, Java, etc.).
* Il gère la communication avec le Frontend.
* Il gère la logique du traitement des requêtes, le contrôle des droits d'accès de l'utilisateur (**authentification et autorisation**), l'exécution de la **logique métier** (calculs, vérification, automatisation) et la préparation d'une requête à destination de la base de données.
* Le Backend et l'API agissent comme un **cerveau** qui comprend la demande du client et sait où la diriger pour qu'elle puisse ressortir une réponse.

---

## 3. Communication et Sécurité

### Sockets
Les **sockets** sont l'intermédiaire entre le client et le serveur, permettant un **échange de données dans les deux sens**.
* Il faut les comparer à une **prise** que l'on va brancher, permettant de faire circuler les données.
* Le serveur utilise une **socket d'écoute** et le client une **socket de connexion**.
* La communication peut être fermée à la fin de l'échange.
* Les échanges se font sur les protocoles **TCP** et **IP** ou **UDP** (qui privilégie la rapidité). Pour une application web, on passe par **HTTP** ou **HTTPS**.

### API (Application Programming Interface)
L'API est l'interface qui va permettre de **connecter plusieurs bases de données ou des programmes entre elles** afin de leur permettre d'intégrer ce qu'elles récoltent dans une architecture déjà établie.
* **Protocoles d'API** :
    * **REST** : Le plus courant, basé sur l'HTTP.
    * **SOAP** : Le plus ancien, basé sur l'HTML.
    * **GraphQL** : Récupère exactement les données souhaitées.
    * **gRPC** : Très rapide pour la communication entre services.
* **Bonnes pratiques pour les API** : documentation, sécurité, versionnage, code de réponse précis et optimisation.

### Sécurisation des Échanges
Le protocole **HTTPS** (HyperText Transfer Protocol Secure) a pour but de **sécuriser les échanges** sur le web entre le serveur et le client, via un chiffrement **SSL** et **TLS**. Il assure trois choses :
1.  L'**authentification** du serveur via un certificat numérique.
2.  Le **chiffrement des données** pour éviter les espions.
3.  L'**intégrité des données** (vérifier que les données n'ont pas été perdues
