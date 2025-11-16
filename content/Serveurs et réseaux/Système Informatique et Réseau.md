# Système Informatique et Réseau

## Adressage et résolution

## Ipv4/IPv

### Principe de l'Adresse IP
Une adresse IP (Internet Protocol) est un numéro d'identification unique attribué à chaque appareil
connecté à un réseau.
Elle fonctionne comme une adresse postale : elle permet d'envoyer des données au bon
destinataire et de savoir d'où elles proviennent.
### IPv4 (Internet Protocol version 4)
- C'est la quatrième version du
Protocole Internet et la première à
avoir été largement déployée,
lancée en 1983.
- Elle utilise un format d'adresse
de  32 bits , ce qui permet environ
4,3 milliards d'adresses uniques.
- Exemple d'adresse IPv : 192.168.10.150.

## IPv6 (Internet Protocol version 6)
- C'est la nouvelle version du Protocole Internet,
conçue pour résoudre les limites de l'IPv4,
notamment l'épuisement des adresses.
- Elle utilise un format d'adresse de  128 bits ,
offrant un nombre considérablement plus grand
d'adresses uniques.
- Exemple d'adresse IPv6: 3002:0bd6:0000:0000:0000:ee00:0033:

## ARP / MAC Address


Principe de la MAC Adress :
- Utilisée pour la
communication  uniquement sur le
réseau local  (ex: entre votre PC et
votre box Internet).
- Format : 6 blocs de caractères
hexadécimaux (ex: 00:1A:2B:3C:4D:5E).
L'adresse MAC est un identifiant
matériel unique et permanent pour
chaque appareil. À l'inverse, l'adresse IP
est temporaire, car elle est attribuée à
l'appareil uniquement lorsqu'il se
connecte à un réseau spécifique


Protocole ARP (Address Resolution Protocol)
- ARP est le "traducteur" qui fait le lien entre une
adresse IP et une adresse MAC sur un réseau
local.C'est un protocole qui permet de retrouver
une adresse MAC à partir d'une adresse IP.
- Quand un appareil veut parler à une adresse IP
locale (ex: 192.168.1.15), il envoie une requête ARP
sur le réseau qui demande : " Qui a cette adresse
IP? Donnez-moi votre adresse MAC! "
- L'appareil concerné répond, permettant ainsi
d'établir la communication directe au niveau
matériel.

## Masque

Une adresse IP se divise en deux parties :


**Adresse réseau** : commune à tous les appareils du même réseau.
**Adresse hôte** : unique à chaque appareil.
**Exemple** :
178.121.100.1 et 178.121.234.2 partagent le même réseau.
 Adr esse réseau : **178.121.0.**
 Masque associé : **255.255.0.**
Le masque (4 octets) permet dʼisoler lʼadresse réseau grâce à lʼopérateur booléen **ET** appliqué entre
lʼadresse IP et le masque.
En binaire :


Adresse hôte : 10110010.11110010.1100100.
Masque : 11111111.11111111. 00000000.
Adresse réseau : 10110010.11110010.00000000.

Soit **178.121.0.0** une fois reconverti en décimal.

## Passerelle

Une passerelle est un outil informatique qui a pour but de relier les différents réseaux entre eux et
dʼ ajouter un niveau de sécurité supplémentaire. La passerelle la plus couramment utilisée est le routeur
aussi appelé “boxˮ. Dans le schéma ci-dessous, nous avons deux réseaux indépendants, si un portable du
premier réseau venait à vouloir communiquer avec un portable du second réseau, il passera par le routeur
qui se chargera du routage des paquets afin de lʼenvoyer à la bonne personne. Cʼest aussi à ce niveau là
que se trouvent généralement un pare-feu pour assurer la sécurité des deux réseaux.

Une passerelle peut aussi se trouver sous la forme dʼ un répéteur

## DHCP

### Quʼest ce que le DHCP?

La fonction Dynamic Host Configuration Protocol
(DHCP) est un protocole client/serveur qui fournit
automatiquement une adresse Internet Protocol
(IP) et dʼautres informations de configuration

### Quʼelle est son utilité?


Chaque appareil sur un réseau TCP/IP doit avoir
une adresse IP unique pour accéder au réseau et à
ses ressources. Sans DHCP, les adresses IP des
nouveaux ordinateurs ou ordinateurs qui sont
déplacés dʼun sous-réseau à un autre doivent être


pertinentes à un hôte IP (par exemple, masque de
sous-réseau et passerelle par défaut).

### Comment ça fonctionne avec un client?

Un client avec DHCP, lors de lʼacceptation dʼune
offre de bail, reçoit :
Adresse IP valide pour le sous-réseau à
laquelle il se connecte.
Options DHCP demandées, qui sont des
paramètres supplémentaires quʼun serveur
DHCP est configuré pour être affecté aux
clients. Parmi les exemples dʼoptions DHCP,
citons Routeur (passerelle par défaut),
Serveurs DNS et Nom de domaine DNS.


configurées manuellement ; les adresses IP des
ordinateurs supprimés du réseau doivent être
récupérées manuellement.
Avec DHCP, lʼ ensemble de ce processus est
automatisé et géré de manière centralisée. Le
serveur DHCP gère un pool dʼadresses IP et loue
une adresse à nʼimporte quel client avec DHCP
lorsquʼil démarre sur le réseau.

## DNS

### Quʼest ce que le DNS?

DNS (Domain Name System) est un protocole
standard qui remplace les noms dʼordinateurs aux
adresses IP (on appelle cela le mappage), ce qui
active la résolution de noms pour les ordinateurs
et les utilisateurs. Par exemple dans les réseaux
Windows, DNS est le service de résolution de
noms par défaut.

### Il existe 4 types de serveurs DNS impliqués dans le chargement dʼune page web :


- Récurseur DNS : Il fonctionne comme une
bibliothécaire qui suite à une demande part
chercher un livre en particulier dans une
bibliothèque. Il reçoit donc les requêtes et fait
des requêtes supplémentaires pour la requêtes
DNS
- Serveur de noms TLD : Cette partie du serveur
contient le TLD (Top Level Domain), il peut être
vu comme le rayonnage spécifique dans un
bibliothèque et cherche la dernière partie du
nom dʼhôte.

### Comment fonctionne le DNS?


Le processus de résolution DNS implique la
conversion d'un nom d'hôte (par exemple,
http://www.example.com) en adresse IP « au format
informatique » (par exemple, 192.168.1.1). Chaque
appareil relié à Internet se voit attribuer une telle
adresse. Cette dernière permet de trouver
l'appareil approprié sur Internet, de la même
manière qu'une adresse dans une rue permet de
trouver un domicile.


Serveur non racine : Cʼ est la première étape
qui sert à la traduction des noms dʼhôtes pour
quʼils soient lisible pour un humain en adresse
IP. Cʼ est comme une catégorie dʼ une
bibliothèque et envoie les différents rayons.
Serveur de noms de références : Cʼ est la
dernière étape, elle est comme un dictionnaire
qui contient la définition de chaque mot pour
trouver lʼ adresse spécifique demander par
lʼutilisateur.

### Les avantages du serveur DNS?

Le DNS a de nombreux avantages dans le réseau : Sécuriser les mises à jour et la réplication des données
DNS, inscription automatique et mises à jour des enregistrements DNS clients, garantit lʼintégrité et


lʼauthenticité des données, ce qui empêche les attaques telles que lʼempoisonnement du cache, résout
efficacement les noms en dehors du réseau local en transférant des requêtes.



