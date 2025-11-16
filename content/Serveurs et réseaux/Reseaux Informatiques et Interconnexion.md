# Réseaux Informatiques et Interconnexion

## 1. Introduction Générale

Un **réseau informatique** est un ensemble d'appareils (ordinateurs,
smartphones, serveurs, imprimantes) interconnectés afin de partager des
données et des ressources.\
Dans le monde professionnel, cela permet par exemple de partager des
fichiers, utiliser des imprimantes communes ou communiquer plus
facilement.

L'**interconnexion des réseaux** consiste à relier plusieurs réseaux
entre eux pour former un ensemble plus vaste :\
- un réseau local d'entreprise relié à Internet,\
- des bureaux distants connectés entre eux,\
- ou encore des réseaux privés reliés via VPN.

Les réseaux modernes descendent de **ARPANET** (années 1960), première
ébauche d'Internet. Depuis, ils sont devenus essentiels : cloud,
visioconférences, objets connectés, jeux en ligne...

------------------------------------------------------------------------

## 2. LAN -- WAN -- Internet

### **LAN (Local Area Network)**

Un LAN couvre une zone géographique limitée (maison, école,
entreprise).\
Il relie des appareils comme :\
- ordinateurs,\
- imprimantes,\
- téléphones,\
- serveurs internes.

Caractéristiques : rapide, sécurisé, administré par une seule
organisation.\
Exemple : le Wi-Fi d'une université.

------------------------------------------------------------------------

### **WAN (Wide Area Network)**

Un WAN relie plusieurs LAN sur de longues distances : villes, pays,
continents.\
Il s'appuie sur : fibre optique, câbles, satellites, opérateurs
télécoms.

Exemple : les différents sites d'une entreprise reliés entre eux.

Internet est lui-même un **immense WAN**.

------------------------------------------------------------------------

### **Internet : le réseau des réseaux**

Internet interconnecte des millions de LAN et WAN grâce aux **protocoles
standards**, notamment **TCP/IP**.

-   **IP** attribue une adresse unique aux appareils.\
-   **TCP** assure la fiabilité et l'ordre des données.

Le fonctionnement repose sur le **packet switching** : chaque message
est découpé en paquets envoyés par des chemins différents et
reconstruits à l'arrivée.

**Exemple** :\
1. Ton mail est découpé en paquets.\
2. Ils passent par ton routeur LAN.\
3. Traversent des WAN via des opérateurs.\
4. Arrivent au LAN des serveurs Gmail.\
5. TCP réassemble le message correctement.

------------------------------------------------------------------------

## 3. Segmentation et Organisation des Réseaux

La segmentation vise à découper un réseau en **sous-réseaux isolés**,
afin d'améliorer la **sécurité**, les **performances** et le
**contrôle**.

### **Définition du LAN**

Un LAN est limité géographiquement et relie des appareils internes via
Ethernet ou Wi-Fi.

------------------------------------------------------------------------

### **VLAN (Virtual LAN)**

Un **VLAN** permet de créer des réseaux virtuels indépendants sur la
même infrastructure physique.

**Exemple dans une université :**\
- VLAN 10 : Administration\
- VLAN 20 : Professeurs\
- VLAN 30 : Étudiants

Ainsi, un étudiant ne peut pas accéder aux ressources des professeurs
même s'ils utilisent le même switch.

#### **Avantages des VLAN :**

-   **Sécurité renforcée**\
    Un virus sur le VLAN étudiant ne touche pas les serveurs
    administratifs.\
-   **Contrôle d'accès amélioré**\
    Ex. : seuls les RH peuvent accéder au serveur de paie.\
-   **Meilleures performances**\
    Moins de trafic inutile entre segments.\
-   **Conformité facilitée** (RGPD, audis, etc.)\
-   **Surveillance accrue**\
    Pare-feux entre segments, journaux d'accès.\
-   **Gestion des menaces internes**\
    Détection de comportements anormaux.\
-   **Isolation et priorisation**\
    Segments critiques (médecine, production industrielle...) mieux
    sécurisés.

------------------------------------------------------------------------

## 4. NAT / PAT (Network Address Translation)

### **Définition**

Le **NAT** permet à plusieurs appareils d'un LAN de partager **une seule
adresse IP publique**.\
Le **PAT** associe des *ports* à chaque connexion pour différencier les
appareils.

**Pourquoi ?**\
Car il n'existe que **4,3 milliards d'adresses IPv4**, insuffisant pour
tous les appareils du monde.

### **Exemple --- à la maison**

-   1 seule IP publique pour la box.\
-   Mais tous les appareils (PC, téléphones, TV) accèdent à Internet
    grâce au NAT/PAT.

### **Exemple --- en entreprise**

-   200 ordinateurs → 1 seule adresse publique.\
-   Le routeur gère les traductions d'adresses.

### **Fonctionnement simplifié**

1.  Ton PC envoie un paquet (IP privée).\
2.  Le routeur remplace l'adresse par l'IP publique.\
3.  Il stocke une table de correspondance.\
4.  Il renvoie la réponse au bon appareil.

### **Types de NAT**

-   NAT statique (1:1)\
-   NAT dynamique (pool d'adresses)\
-   PAT (NAT avec ports) --- *le plus courant*

### **Limites**

-   Certains services : VoIP, jeux, P2P\
-   Traçabilité plus complexe

------------------------------------------------------------------------

## 5. Routage de Base

### **Définition**

Le **routage** choisit le meilleur chemin pour transporter les paquets
d'un point à un autre.

### **Pourquoi c'est essentiel ?**

-   Optimise la vitesse et évite la congestion\
-   Assure la continuité même en cas de panne\
-   Permet la communication entre réseaux

### **Le routeur --- rôle**

-   Choisit le meilleur chemin\
-   Transmet les paquets\
-   Répartit la charge entre plusieurs routes

Il s'appuie sur une **table de routage**, mise à jour manuellement ou
automatiquement.

------------------------------------------------------------------------

### **Types de routage**

-   **Statique** : routes configurées à la main\
-   **Dynamique** : routes mises à jour automatiquement

### **Protocoles de routage**

**IGP (interne)**\
- RIP\
- OSPF

**EGP (externe)**\
- BGP (fondement d'Internet)

Les routeurs utilisent des algorithmes :\
- vecteur de distance\
- état de lien

------------------------------------------------------------------------

## 6. Conclusion Générale

Les réseaux --- LAN, WAN, Internet --- constituent la **colonne
vertébrale du monde numérique**.\
L'interconnexion, permise par TCP/IP, le routage, les VLAN, le NAT/PAT,
assure une communication fiable, rapide et sécurisée.

Dans un environnement dominé par le cloud, les objets connectés et l'IA,
comprendre les réseaux est essentiel pour comprendre le fonctionnement
même d'Internet et des infrastructures modernes.

Un réseau bien conçu n'est plus seulement un outil, mais un **levier de
sécurité, de performance et d'innovation**.
