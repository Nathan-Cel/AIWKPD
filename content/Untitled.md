# Réseaux Informatiques et Interconnexion

Introduction générale

Un réseau informatique est un ensemble d’ordinateurs et de périphériques connectés  
entre eux pour partager des informations et des ressources. Dans une entreprise, cela  
permet aux employés d’accéder à des fichiers communs, d’utiliser des imprimantes  
partagées ou encore de communiquer plus facilement.

Mais les réseaux ne restent pas isolés. Grâce à l’interconnexion, il est possible de  
relier plusieurs réseaux entre eux pour former un plus grand ensemble. Par exemple,  
le réseau interne d’une entreprise peut être connecté à Internet, ce qui permet  
d’échanger avec des clients, des partenaires ou d’accéder à des services en ligne.

L’histoire des réseaux remonte aux années 1960 avec ARPANET, l’ancêtre d’Internet,  
qui reliait des universités et centres de recherche. Depuis, les réseaux ont évolué  
jusqu’à devenir indispensables dans notre quotidien : visioconférences, cloud, jeux  
en ligne ou encore objets connectés.

## Présentation LAN – WAN – Internet

### LAN (Local Area Network)

Tout d’abord, commençons par le LAN, c’est-à-dire le _Local Area Network_ , en français «  
réseau local ».  
Un LAN est limité géographiquement : il peut couvrir une maison, une école, ou encore une  
entreprise.

Il permet de connecter entre eux des ordinateurs, des imprimantes, des téléphones ou  
même des serveurs internes.

De plus, un LAN est rapide, sécurisé, et surtout géré par une seule organisation.  
Par exemple, le Wi-Fi de notre faculté est un LAN : il relie nos ordinateurs et nos  
smartphones au réseau interne de l’université.

### WAN (Wide Area Network)

Ensuite, voyons le WAN, qui signifie _Wide Area Network_ , ou « réseau étendu ».  
Contrairement au LAN, un WAN couvre de très grandes zones : des villes, des pays, voire  
plusieurs continents.

Autrement dit, il relie plusieurs LAN entre eux grâce à des opérateurs de  
télécommunications, en utilisant la fibre optique, les câbles ou encore les satellites.  
Par exemple, lorsqu’une entreprise possède des bureaux dans plusieurs villes, c’est un  
WAN qui relie tous ses réseaux locaux.

Et en réalité, Internet lui-même est un gigantesque WAN.

### Internet

Enfin, parlons d’Internet, qui est le plus grand réseau mondial.  
En réalité, Internet est ce qu’on appelle un _réseau de réseaux_. Il relie des millions de  
réseaux locaux (LAN) et étendus (WAN) grâce à des règles communes, qu’on appelle des  
_protocoles_.

Selon Cloudflare ( _How does the Internet work_ , source : cloudflare.com), ces protocoles  
permettent à des données de voyager d’un réseau à l’autre sans problème de compatibilité.

Pour être plus précis, Internet repose sur la suite TCP/IP :

● IP (Internet Protocol) donne une adresse à chaque appareil connecté. C’est un peu  
comme une adresse postale pour savoir où envoyer les données.

● TCP (Transmission Control Protocol) vérifie que les données arrivent complètes,  
sans erreur et dans le bon ordre.

C’est ce qu’explique TechTarget ( _What is TCP/IP_ , source : techtarget.com).

De plus, Internet fonctionne grâce au principe du “packet switching” :  
Quand tu envoies un message, il est découpé en petits morceaux appelés “paquets”.  
Ces paquets voyagent chacun par des chemins différents et sont réassemblés à l’arrivée.

Ce mécanisme, décrit par Cloudflare ( _How does the Internet work_ , source : cloudflare.com),  
rend Internet rapide et efficace.

Si on prend un exemple concret :  
Lorsque tu envoies un mail depuis ton ordinateur connecté à ton LAN :

1. Ton message est transformé en paquets.
2. Ces paquets sont transmis par ton routeur.
3. Ils traversent plusieurs WAN via des opérateurs.
4. Ils arrivent finalement sur un autre LAN, par exemple celui des serveurs Gmail.
5. TCP se charge ensuite de reconstituer correctement le message pour ton  
    destinataire.

Enfin, un mot sur l’histoire, car c’est important de comprendre d’où vient Internet.  
À l’origine, dans les années 1960, il existait un réseau expérimental aux États-Unis, appelé  
ARPANET.  
Puis, en 1983 , un moment clé est arrivé : tous les ordinateurs de ce réseau sont passés au  
protocole TCP/IP.

D’après l’Internet Society ( _A Brief History of the Internet_ , source : internetsociety.org), c’est  
cette date que l’on considère comme la “naissance” de l’Internet moderne.

### Schéma explicatif

Pour bien visualiser cela, regardons le schéma suivant :

![[Pasted image 20251115130434.png]]

Comment le lire?

```
● En bas, on retrouve le LAN, avec un switch qui relie plusieurs PC, des ordinateurs
portables via le Wi-Fi, et un serveur interne.
```

```
● Au milieu, il y a le routeur et les pare-feu qui sécurisent les échanges. C’est eux qui
permettent de sortir du réseau local.
```

```
● Puis, les données passent dans le WAN, représenté ici par un nuage, qui relie
différents réseaux grâce aux opérateurs.
```

```
● Enfin, à gauche et à droite, on voit des ordinateurs distants (chez soi ou en
déplacement) qui peuvent accéder au réseau via des connexions sécurisées comme
les VPN.
```

Donc, ce schéma illustre parfaitement Internet : une interconnexion mondiale de LAN  
reliés entre eux par des WAN, sécurisés par des pare-feu, et accessibles de partout dans le  
monde.

### 3. La segmentation et organisation des réseaux

La segmentation et organisation des réseaux est un processus essentiel pour  
renforcer la sécurité et optimiser les performances des infrastructures informatiques,  
elle **consiste à diviser un réseau en plusieurs sous-réseaux, chacun avec ses propres  
règles d'accès et de contrôle, afin de limiter l'impact des attaques et de protéger les  
données sensibles.**

### Definitions á prendre en compte :

#### LAN (Local Area Network) : Un LAN (réseau local) est un réseau

informatique limité à une petite zone géographique : une maison, une école, un  
bureau, une usine, etc.  
👉 C’est le réseau que tu utilises à l’intérieur d’un bâtiment pour connecter les  
ordinateurs, imprimantes, serveurs, caméras, etc.

#### Caractéristiques :

```
● Zone géographique limitée (quelques mètres à quelques kilomètres max).
● Débit élevé (connexion rapide entre les appareils, souvent en Gbps).
● Propriété privée : le LAN appartient à une organisation (école, entreprise,
particulier).
● Connexion par câbles (Ethernet) ou sans fil (Wi-Fi).
```

```
Exemple d’un réseau LAN d’une maison
```

### VLAN, une des méthodes les plus utilisées :

VLAN (Virtual LAN)

1. Définition

Un VLAN (Virtual Local Area Network) est un réseau local virtuel qui permet de  
regrouper des machines logiquement, même si elles ne sont pas physiquement

connectées au même endroit.  
C’est une segmentation logique d’un réseau physique.

```
● Exemple simple : dans une université, les PC des étudiants, des professeurs et
de l’administration sont tous branchés sur les mêmes commutateurs (switch).
→ Avec des VLAN, on sépare leurs trafics :
○ VLAN 10 = Administration
○ VLAN 20 = Professeurs
○ VLAN 30 = Étudiants
```

Ainsi, même si un étudiant est branché sur la même prise réseau qu’un prof, il ne peut  
pas voir ni interférer avec son trafic.

## Avantages :

**Elle permet de cloisonner les ressources critiques, d'empêcher les accès non  
autorisés et d'améliorer la conformité réglementaire.**

De manière plus précise :

Sécurité renforcée

```
● Propagation limitée → Exemple : un virus attaque un ordinateur étudiant dans
un campus. Grâce aux VLAN, il ne peut pas atteindre les serveurs
administratifs.
● Détection plus facile → Exemple : une tentative de connexion à un serveur de
paie depuis le Wi-Fi invité déclenche une alerte.
● Protection des systèmes critiques → Exemple : un hôpital met ses appareils
médicaux (scanners, IRM) dans un segment isolé, donc inaccessibles depuis
Internet.
● Isolement des réseaux non fiables → Exemple : les visiteurs d’une entreprise
utilisent un Wi-Fi invité séparé, donc ils ne peuvent pas voir les fichiers
internes.
```

Meilleur contrôle d’accès

```
● Gestion des accès → Exemple : seuls les comptables peuvent accéder au
serveur qui contient les factures.
● Restriction pour les tiers → Exemple : une société de maintenance
informatique n’a accès qu’aux serveurs qu’elle gère, pas au reste du réseau.
```

Amélioration des performances

```
● Moins de trafic local → Exemple : dans une école, les imprimantes et les PC
des étudiants sont dans deux segments différents → les flux des étudiants ne
ralentissent pas l’accès des profs aux serveurs pédagogiques.
```

Facilite la conformité réglementaire

```
● Audits limités → Exemple : pour une banque, seuls les serveurs qui stockent
les données bancaires sont audités, pas toute l’infrastructure.
● Simplification légale → Exemple : une entreprise e-commerce isole les bases
de données clients → cela réduit la portée des contrôles RGPD.
```

Visibilité et surveillance accrues

```
● Pare-feu entre segments → Exemple : un pare-feu entre le réseau administratif
et le réseau étudiant enregistre tout passage suspect.
● Journalisation → Exemple : en cas d’intrusion, les logs montrent qu’une
machine du réseau invité a tenté d’accéder au serveur RH.
```

Gestion des menaces internes

```
● Activité suspecte détectée → Exemple : un employé essaie de télécharger en
masse des fichiers confidentiels, l’alerte est déclenchée car son segment n’a
pas ce droit.
```

Priorisation et isolation

```
● Ressources critiques isolées → Exemple : dans une usine, les machines de
production (robots industriels) sont dans un segment très sécurisé, séparé du
réseau bureautique.
● Concentration de la sécurité → Exemple : une entreprise investit plus dans la
sécurité du segment qui héberge son site e-commerce (car critique) que dans
celui du Wi-Fi invité.
```

**_Source : étude par l’Université de Quebec, CESI  
(segmentation-reseau-v1-2-20240501.pdf)_**

## Partie 4 : NAT / PAT (Network Address

## Translation)

1. Définition simple

Le NAT (Network Address Translation) est une technique utilisée par les routeurs pour  
permettre à plusieurs appareils d’un réseau local (LAN) d’accéder à Internet avec une  
seule adresse IP publique.

Sans NAT, chaque appareil (PC, smartphone, imprimante) aurait besoin d’une adresse  
publique unique → impossible car il n’y a pas assez d’IPv4 dans le monde.[kk1]

Le PAT (Port Address Translation) est une forme de NAT qui permet à plusieurs  
appareils de partager la même adresse IP publique, en utilisant des numéros de ports  
pour les distinguer.

2. Pourquoi le NAT/PAT est important?

```
● Économie d’adresses IPv4 : un seul IP publique pour des dizaines d’appareils.
● Sécurité : masque les adresses internes (ex. 192.168.1.10) → plus difficile pour
un pirate d’attaquer directement.
● ⚙Simplicité : facile à gérer, évite d’acheter beaucoup d’IP publiques.
```

3. Exemple concret

À la maison

```
● Tu as une box Internet (Freebox, Livebox, etc.).
● Elle reçoit 1 seule adresse publique de ton fournisseur (FAI).
● Pourtant, ton PC, ton téléphone, ta console et ta TV peuvent tous aller sur
Internet.
● C’est grâce au NAT/PAT dans ta box, qui traduit les adresses privées
(192.168.x.x) en une adresse publique.
```

En entreprise

```
● Une société a 200 ordinateurs.
```

```
● Elle ne paie qu’une adresse publique fournie par l’opérateur.
● Le routeur avec NAT gère les traductions et permet aux employés de se
connecter simultanément à Internet.
```

4. Fonctionnement simplifié
    1. Ton PC (192.168.1.2) envoie un paquet vers Internet.
    2. Le routeur remplace l’adresse privée par l’adresse publique (ex. 102.45.22.1).
    3. Pour savoir à qui renvoyer la réponse, le routeur garde une table de  
        correspondance.
    4. Quand la réponse arrive, il la renvoie au bon PC.

Avec le PAT, il utilise aussi les numéros de ports pour différencier plusieurs  
connexions.

5. Schémas :
6. Types de NAT

```
● NAT statique : 1 adresse privée ↔ 1 adresse publique (ex. un serveur web).
● NAT dynamique : pool d’adresses publiques utilisées selon les besoins.
● PAT (NAT avec ports) : plusieurs adresses privées ↔ 1 adresse publique, grâce
aux ports (le plus courant → box Internet).
```

7. Limites

```
● ❌ Certaines applications (VoIP, jeux en ligne, P2P) peuvent avoir des
problèmes car elles veulent une adresse unique.
● ❌ Rend parfois le suivi des utilisateurs plus difficile (traçabilité).
```

✅ En résumé :  
Le NAT/PAT est indispensable aujourd’hui pour que nos foyers, entreprises et écoles  
puissent connecter de nombreux appareils avec peu d’adresses publiques. C’est à la  
fois une solution économique, pratique et sécurisante, même si elle n’est pas parfaite.

[kk1]Une adresse IPv4 c’est comme une plaque d’immatriculation unique pour chaque  
appareil connecté à Internet.

Le problème : il n’y a que 4,3 milliards d’adresses IPv4 possibles (c’est la limite  
mathématique).

Or, aujourd’hui, il y a beaucoup plus d’appareils (PC, smartphones, tablettes, objets  
connectés, caméras, voitures, etc.).  
👉 Résultat : il n’y a pas assez d’adresses IPv4 pour tout le monde.

### 5. Routage de base

#### Qu’est-ce que le routage?

Le routage est le processus qui permet de sélectionner un chemin dans un réseau  
pour faire circuler les données entre deux machines. Dans un réseau interconnecté, il  
existe souvent plusieurs chemins possibles entre un point A et un point B. Le routage  
sert à déterminer le meilleur chemin, en fonction de critères comme la rapidité, la  
disponibilité ou la capacité du réseau.

#### Les paquets : l’unité de base

Les données ne circulent pas « en bloc » dans un réseau, mais sous forme de  
paquets.  
Un paquet est comme une enveloppe numérique : il contient une partie des données à  
transmettre (ex. : une portion d’un mail, une page web) ainsi que des informations  
essentielles pour le transport, comme l’adresse source, l’adresse de destination et  
parfois un numéro de port.

Le rôle du routage est donc de guider correctement ces paquets vers leur destination,  
même s’ils doivent traverser plusieurs réseaux.

#### Pourquoi le routage est-il important?

```
● Il optimise l’efficacité des communications réseau en choisissant les chemins
les plus rapides et en évitant les zones surchargées.
● Il assure la continuité du service : si un chemin tombe en panne, le routeur
peut en utiliser un autre.
● Il permet à des réseaux distincts de communiquer entre eux, ce qui est
indispensable pour Internet.
```

#### Le routeur : rôle et fonctionnement

Un routeur est l’équipement réseau chargé de mettre en œuvre le routage. Il a trois  
fonctions principales :

1. Déterminer le chemin : choisir la meilleure route selon des critères (délai, capacité,  
    fiabilité).
2. Transférer les données : envoyer les paquets au prochain routeur ou à  
    l’équipement final.
3. Équilibrer la charge : répartir le trafic sur plusieurs chemins pour éviter la  
    congestion.  
    Lorsqu’un paquet arrive, le routeur lit son en-tête (adresse de destination) et consulte sa  
    table de routage. Il y trouve soit une route directe, soit une route par défaut vers un  
    autre routeur. Le processus est répété jusqu’à la destination finale.  
    👉 Exemple : ton ordinateur envoie une requête à un site web. Le paquet passe par le  
    routeur de ton réseau, puis par ton fournisseur d’accès, ensuite par d’autres routeurs

#### intermédiaires, jusqu’au serveur du site. La réponse emprunte le chemin inverse.

#### Types de routage

On distingue deux formes principales :  
● Routage statique : les routes sont configurées manuellement par un  
administrateur. Simple mais peu flexible si le réseau évolue.  
● Routage dynamique : les routeurs mettent à jour automatiquement leurs tables  
en fonction de l’état du réseau (trafic, pannes, nouvelles liaisons). Plus adapté  
aux grands réseaux modernes.

#### Les protocoles de routage

Un protocole de routage définit les règles qui permettent aux routeurs de  
communiquer et d’échanger des informations sur les chemins disponibles.  
Deux grandes familles existent :  
● Protocoles de passerelle interne (IGP – Interior Gateway Protocols) : utilisés à  
l’intérieur d’un système autonome (un réseau géré par une organisation).  
○ RIP (Routing Information Protocol) : ancien protocole basé sur le  
nombre de sauts. Simple mais limité.

○ OSPF (Open Shortest Path First) : plus performant, il cartographie tout  
le réseau pour calculer le chemin le plus court.  
● Protocoles de passerelle externe (EGP – Exterior Gateway Protocols) : utilisés  
entre plusieurs systèmes autonomes.  
○ BGP (Border Gateway Protocol) : protocole clé d’Internet, qui permet  
aux différents réseaux (identifiés par un numéro ASN) d’échanger leurs  
routes à l’échelle mondiale.  
Ces protocoles s’appuient sur des algorithmes de routage, comme :  
● le vecteur de distance (chaque routeur partage régulièrement ses informations  
de routes avec les autres),  
● l’état de lien (chaque routeur construit une carte du réseau et calcule le chemin  
optimal).

#### L’évolution du routage

Au départ, le routage consistait surtout à transporter des paquets entre des LAN, des  
WAN et Internet. Mais avec les avancées technologiques, il a dû s’adapter.  
● Les fournisseurs de cloud (AWS, Azure, Google Cloud, etc.) hébergent  
aujourd’hui des serveurs et des applications accessibles à distance.  
● Les entreprises utilisent de plus en plus des réseaux hybrides, combinant  
leurs infrastructures locales (datacenters) et des services cloud.  
● Les routeurs modernes doivent donc gérer des communications entre des  
environnements très différents : réseau interne, Internet et cloud.  
👉 Le routage est ainsi devenu plus complexe et flexible, mais aussi plus essentiel  
que jamais pour garantir une connectivité continue et fiable dans notre monde  
numérique.

##### En conclusion : les réseaux informatiques constituent aujourd’hui la colonne

vertébrale de notre monde numérique. Qu’il s’agisse de simples réseaux locaux (LAN)  
ou de vastes infrastructures mondiales (WAN, Internet), leur rôle est de permettre la  
communication, le partage et la sécurité des données entre utilisateurs, appareils et  
organisations.

L’interconnexion de ces réseaux — rendue possible par des technologies comme  
TCP/IP, le routage, le NAT/PAT ou encore la segmentation via VLAN — assure la  
continuité des échanges et la protection des ressources.

Ces mécanismes garantissent que les informations circulent efficacement tout en  
maintenant un haut niveau de fiabilité, de performance et de sécurité.

Aujourd’hui, dans un contexte où tout est connecté (cloud, objets intelligents,  
mobilité, IA), la maîtrise des réseaux et de leur interconnexion est devenue  
incontournable. Comprendre leur fonctionnement, c’est comprendre les fondations  
d’Internet et du monde numérique moderne.

En somme, un réseau bien conçu n’est pas seulement un moyen de connexion, mais  
un véritable levier de performance, de sécurité et d’innovation pour les entreprises,  
les institutions et les particuliers.

https://aws.amazon.com/fr/what-is/routing/#:~:text=Le%20routage%20est%20le%20processus,par%20de%20nombreux%20chemins%20diff%C3%A9rents.