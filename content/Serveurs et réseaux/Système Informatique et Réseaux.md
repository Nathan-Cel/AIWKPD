# Système Informatique et Réseau

## 1. Adressage IP : Concepts Essentiels

### Principe d'une Adresse IP

Une **adresse IP** est un identifiant unique attribué à chaque appareil
connecté à un réseau.\
Elle fonctionne comme une adresse postale : elle permet d'acheminer les
données au bon destinataire.

------------------------------------------------------------------------

### IPv4 (Internet Protocol version 4)

-   Version largement déployée depuis **1983**\
-   Format de **32 bits** → environ **4,3 milliards d'adresses**\
-   Exemple : `192.168.10.150`

------------------------------------------------------------------------

### IPv6 (Internet Protocol version 6)

-   Créée pour résoudre l'épuisement des adresses IPv4\
-   Format de **128 bits** → nombre quasi illimité d'adresses\
-   Exemple : `3002:0bd6:0000:0000:0000:ee00:0033:0000`

------------------------------------------------------------------------

## 2. ARP & Adresse MAC

### Adresse MAC (Media Access Control)

-   Identifiant **matériel et permanent** d'une carte réseau\
-   Utilisée **uniquement sur le réseau local (LAN)**\
-   Format : `00:1A:2B:3C:4D:5E`

**Différence avec l'adresse IP :**\
- IP = attribuée par le réseau (variable)\
- MAC = propre à l'appareil (fixe)

------------------------------------------------------------------------

### Protocole ARP (Address Resolution Protocol)

ARP sert de **pont entre l'adresse IP et l'adresse MAC**.

Fonctionnement : 1. Un appareil veut contacter une IP locale (ex.
`192.168.1.15`)\
2. Il envoie : *« Qui possède cette IP ? Donnez-moi votre MAC ! »*\
3. La machine concernée répond\
4. La communication locale peut commencer

------------------------------------------------------------------------

## 3. Masque de Sous-Réseau

Une adresse IP comporte : - **Adresse réseau** : commune au sous-réseau\
- **Adresse hôte** : unique à chaque machine

Exemple :\
IP : `178.121.100.1`\
Masque : `255.255.0.0`\
→ Adresse réseau : **178.121.0.0**

Le masque permet d'obtenir l'adresse réseau grâce à l'opération **ET
binaire**.

------------------------------------------------------------------------

## 4. Passerelle (Gateway)

La **passerelle**, souvent un **routeur/box**, relie plusieurs réseaux
entre eux.\
Elle permet : - la communication entre LAN distincts\
- la connexion vers Internet\
- l'ajout de sécurité via un pare-feu intégré

Exemple :\
Un PC du réseau A veut parler à un PC du réseau B → les paquets passent
par la passerelle.

------------------------------------------------------------------------

## 5. DHCP (Dynamic Host Configuration Protocol)

### Qu'est-ce que DHCP ?

DHCP attribue automatiquement : - une adresse IP\
- un masque\
- une passerelle\
- un DNS

**Objectif :** éviter les configurations manuelles répétitives.

------------------------------------------------------------------------

### Fonctionnement côté client

Lorsqu'un client rejoint un réseau : 1. Il demande une adresse\
2. Le serveur DHCP lui **propose un bail**\
3. Le client reçoit : - une IP valide\
- la passerelle\
- les serveurs DNS\
- des options supplémentaires

Le tout est automatisé via un **pool d'adresses** centralisé.

------------------------------------------------------------------------

## 6. DNS (Domain Name System)

### Rôle du DNS

Le DNS convertit des **noms de domaine** (ex. `www.example.com`) en
**adresses IP**.\
Il est indispensable pour naviguer sur Internet sans mémoriser les
adresses.

------------------------------------------------------------------------

### Les 4 serveurs DNS impliqués dans une résolution

#### 1. Récurseur DNS

Reçoit la requête du client et effectue des recherches supplémentaires.

#### 2. Serveur racine

Première étape de la résolution, il oriente vers la bonne catégorie (ex.
`.com`, `.fr`).

#### 3. Serveur TLD (Top Level Domain)

Cherche la dernière partie du nom (ex. « .com » dans `example.com`).

#### 4. Serveur de noms faisant autorité

Dernière étape, il fournit l'adresse IP exacte.

------------------------------------------------------------------------

### Comment fonctionne la résolution DNS ?

1.  Le PC demande à traduire `www.example.com`\
2.  Le récurseur consulte les serveurs DNS\
3.  Le serveur faisant autorité retourne l'adresse IP\
4.  Le navigateur peut alors contacter le bon serveur web

------------------------------------------------------------------------

### Avantages du DNS

-   Mise à jour automatique\
-   Réplication sécurisée\
-   Vérification d'intégrité\
-   Protection contre l'empoisonnement DNS\
-   Résolution de noms en dehors du réseau local

------------------------------------------------------------------------

Ce document reformulé synthétise les notions essentielles d'adressage,
de routage local, d'automatisation et de résolution de noms dans un
système informatique moderne.
