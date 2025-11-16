# HTTP/HTTPS et API

Protocoles et Architecture Web
# Concepts Fondamentaux
## HTTP

HyperText Transfer Protocol -
protocole de communication du
web

## HTTPS

HTTP Secure - version sécurisée
avec chiffrement TLS

## API

Application Programming Interface -
interface permettant aux logiciels
de communiquer

## TLS

Transport Layer Security - protocole de sécurisation des
communications

## REST

Representational State Transfer - architecture pour les
services web

# Historique
## HTTP/1.0
1996 : Une requête par connexion

## HTTP/1.1
1999 : Connexions persistantes

## HTTP/2
2015 : Multiplexage

## HTTP/3
QUIC/UDP pour latence réduite

# Anatomie d'une Requête HTTP
1. Ligne de Requête

Méthode + URL + Version HTTP
GET /index.html HTTP/1.

2. En-têtes

Métadonnées : Host, User-Agent, Accept

3. Corps

Données envoyées (POST, PUT)

# Anatomie d'une Réponse HTTP
1. Ligne de Statut
Version HTTP + Code + Message
HTTP/1.1 200 OK

2. En-têtes
Content-Type, Content-Length, Cache-Control

3. Corps
Contenu demandé : HTML, JSON, données

# Méthodes HTTP et Propriétés

## GET
Lire une ressource. Sécuritaire, idempotent.

## POST
Créer une ressource. Envoyer des données au serveur.

## PUT/PATCH
Mettre à jour une ressource. Idempotents.

## DELETE
Supprimer une ressource. Idempotent.

# Codes de Statut HTTP

## 1xx
Information

## 2xx
Succès : 200 OK, 201 Created

## 3xx
Redirection : 301 Moved

## 4xx
Erreur Client : 404 Not Found, 403
Forbidden

## 5xx
Erreur Serveur : 500 Internal Error

# API Web et HTTP

Une API Web (REST) utilise HTTP comme protocole de transport. Elle reprend tous les concepts HTTP : ressources identifiées par URL, méthodes HTTP pour agir, codes de statut pour le résultat, données en JSON.

Ressources
Identifiées par URL

Opérations
GET, POST, PUT, DELETE

Réponses
Codes HTTP et données JSON

# En-têtes HTTP
## Requête (Client ³ Serveur)

Authorization
Cookie
Accept
User-Agent

## Réponse (Serveur ³ Client)

Content-Type
Set-Cookie
Cache-Control
HSTS

# TLS (Transport Layer Security)

Le Transport Layer Security (TLS), successeur de SSL, assure une communication sécurisée sur Internet à travers :

# Confidentialité
Chiffrement des données

# Intégrité
Détection des altérations

# Authentification
Vérification du serveur via certificat

Le handshake TLS est un processus crucial qui négocie la version du protocole, les algorithmes de chiffrement et le certificat du
serveur, puis génère les clés de session. Après cette étape, tout le contenu HTTP (y compris les en-têtes) est entièrement
chiffré, garantissant ainsi la sécurité des échanges.

#SNI (Server Name Indication)

## Problème
Plusieurs sites sur une même IP ³ comment choisir le bon certificat
?

## Définition
Extension TLS permettant au client de préciser le nom de domaine
lors du handshake.

## Limite
Le domaine est visible en clair (mais pas le contenu) ³ ECH peut
améliorer la confidentialité.

Séquence typique

1. Client envoie SNI
2. Serveur renvoie certificat
3. TLS sécurisé
4. HTTP envoyé dans le tunnel chiffré

# CORS (Cross-Origin Resource Sharing)

## Définition
Permet l'accès à des ressources sur une autre origine

## Fonction
Sécurise les requêtes cross-Origin via XMLHttpRequest ou Fetch

## En-têtes clés CORS

- Access-Control-Allow-Origin
- Access-Control-Allow-Credentials

## Problème résolu
Politique de même origine (Same-Origin Policy)

# Stateful vs Stateless

## Stateful

- Serveur conserve l'étatentre requêtes.
- Dépend des sessions/cookies.
- Exemples : banques, jeux en ligne.

## Stateless

- Serveur ne conserve pas l'état.
- Requêtes indépendantes, plus scalable.
- Exemples : API REST.

## Différences

Stateful : état conservé, complexe, moins scalable, vulnérable
Stateless : pas d'état, simple, scalable, plus sûr.
