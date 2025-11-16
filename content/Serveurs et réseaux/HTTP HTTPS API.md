# HTTP, HTTPS et API

## 1. Concepts Essentiels

### **HTTP**

Le *HyperText Transfer Protocol* est le protocole de base utilisé sur le
Web pour échanger des données entre un client et un serveur.

### **HTTPS**

Version sécurisée de HTTP. Elle ajoute une couche de chiffrement grâce à
TLS afin de garantir confidentialité et intégrité.

### **API**

Une *Application Programming Interface* permet à différents logiciels de
communiquer entre eux via un ensemble de règles et de formats définis.

### **TLS**

Le *Transport Layer Security* chiffre les communications, authentifie
les serveurs et protège les données transportées.

### **REST**

*Representational State Transfer* : un style architectural pour
concevoir des API simples, scalables et basées sur les ressources.

------------------------------------------------------------------------

## 2. Évolution des Versions HTTP

-   **HTTP/1.0 (1996)** --- Une requête par connexion.\
-   **HTTP/1.1 (1999)** --- Connexions persistantes, meilleures
    performances.\
-   **HTTP/2 (2015)** --- Multiplexage pour envoyer plusieurs requêtes
    simultanément.\
-   **HTTP/3** --- Basé sur QUIC (UDP) pour réduire la latence et
    améliorer la fiabilité.

------------------------------------------------------------------------

## 3. Structure d'une Requête HTTP

1.  **Ligne de requête**\
    Exemple : `GET /index.html HTTP/1.1`

2.  **En-têtes**\
    Métadonnées indiquant le type de client, le domaine ciblé, les
    formats acceptés, etc.

3.  **Corps**\
    Utilisé pour envoyer des données (POST, PUT...).

------------------------------------------------------------------------

## 4. Structure d'une Réponse HTTP

1.  **Ligne de statut**\
    Exemple : `HTTP/1.1 200 OK`

2.  **En-têtes**\
    Type de contenu, taille, directives de cache, cookies...

3.  **Corps**\
    Contenu retourné (HTML, JSON, données brutes...).

------------------------------------------------------------------------

## 5. Méthodes HTTP

-   **GET** --- Récupérer une ressource. *Sûr et idempotent.*\
-   **POST** --- Créer ou envoyer des données au serveur.\
-   **PUT / PATCH** --- Mettre à jour une ressource. *Idempotents.*\
-   **DELETE** --- Supprimer une ressource. *Idempotent.*

------------------------------------------------------------------------

## 6. Codes de Statut HTTP

-   **1xx --- Information**\
-   **2xx --- Succès** : `200 OK`, `201 Created`\
-   **3xx --- Redirection** : `301 Moved Permanently`\
-   **4xx --- Erreurs Client** : `404 Not Found`, `403 Forbidden`\
-   **5xx --- Erreurs Serveur** : `500 Internal Server Error`

------------------------------------------------------------------------

## 7. API Web et HTTP

Les API REST exploitent les concepts HTTP :\
- **Ressources** identifiées par des URL\
- **Méthodes** : GET, POST, PUT, DELETE\
- **Réponses** : codes HTTP + données (souvent JSON)

------------------------------------------------------------------------

## 8. Principaux En‑têtes HTTP

### Côté Client → Serveur

-   `Authorization`\
-   `Cookie`\
-   `Accept`\
-   `User-Agent`

### Côté Serveur → Client

-   `Content-Type`\
-   `Set-Cookie`\
-   `Cache-Control`\
-   `Strict-Transport-Security (HSTS)`

------------------------------------------------------------------------

## 9. Sécurité : TLS

TLS fournit :\
- **Confidentialité** grâce au chiffrement\
- **Intégrité** pour garantir l'absence de modifications\
- **Authentification** via les certificats

Le **handshake TLS** négocie les algorithmes, vérifie le certificat puis
génère une clé de session. Après cela, tout le trafic HTTP est chiffré.

------------------------------------------------------------------------

## 10. SNI (Server Name Indication)

### Problème

Plusieurs sites hébergés sur une même IP doivent présenter le bon
certificat.

### Fonction

Le client indique le nom de domaine lors du handshake TLS.

### Limite

Le nom de domaine reste visible en clair. L'ECH vise à le masquer.

------------------------------------------------------------------------

## 11. CORS (Cross‑Origin Resource Sharing)

Mécanisme permettant à une page Web d'accéder à une ressource située sur
une origine différente.

En‑têtes importants :\
- `Access-Control-Allow-Origin`\
- `Access-Control-Allow-Credentials`

CORS complète la **Same-Origin Policy**.

------------------------------------------------------------------------

## 12. Stateful vs Stateless

### **Stateful**

-   Le serveur conserve un état (sessions, contexte).\
-   Utile pour applications sensibles (banques, jeux).\
-   Moins scalable.

### **Stateless**

-   Chaque requête est indépendante.\
-   Plus simple, plus scalable.\
-   Concept clé des API REST.

------------------------------------------------------------------------
