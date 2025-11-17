# 🌐 Tendances Modernes en Architecture Réseau et Cybersécurité

Lien vers le PDF : https://aivancity-my.sharepoint.com/:b:/g/personal/estelle_baya_aivancity_education/EaqLpmqK5ydIsltYxoOtwzoBj5nA96RlJDdiNZv_tWoSgw?e=PlJOwE

## BYOD (Bring Your Own Device)

Le **BYOD** est une politique d’entreprise où les employés utilisent leurs appareils **personnels** (smartphones, tablettes, PC portables) pour accéder aux ressources professionnelles. Ce concept, popularisé depuis les années 2010, présente des enjeux stratégiques : il permet de gagner en flexibilité et de réduire les coûts matériels (l’entreprise n’achète pas d’appareils). Par exemple, la CNIL a publié en 2013 des recommandations sur le BYOD.

### Avantages
* Le BYOD augmente la **productivité** et la **satisfaction** des utilisateurs (travail à distance facilité), et attire les talents sensibles à la mobilité.
* Il permet souvent une **réduction des coûts** informatiques et une meilleure **réactivité** (l’utilisateur peut travailler avec l’outil de son choix, à tout moment).

### Risques
* La **sécurité** est le principal défi : vol ou perte d’appareil, logiciels malveillants, accès non autorisés aux données de l’entreprise.
* Le mélange d’usage personnel et professionnel complexifie la gestion et **accroît la surface d’attaque**.
* Des failles ou un appareil compromis peuvent mener à des **fuites de données sensibles**.

### Exemples et Bonnes Pratiques
* Pour en limiter les risques, il est conseillé d’établir une **politique BYOD claire** (définir quels usages sont autorisés, imposer mots de passe robustes, chiffrement, authentification forte, etc.).
* Utiliser des solutions de **MDM** (Mobile Device Management) pour contrôler les terminaux.
* **Former/sensibiliser** les utilisateurs aux bonnes pratiques.
* Imposer l’usage d’un **VPN chiffré** ou verrouiller l’accès aux données de l’entreprise lorsque l’utilisateur n’est pas authentifié.

## Cloud (IaaS, PaaS, SaaS – public, privé, hybride)

Le **cloud computing** désigne la fourniture de ressources informatiques (serveurs, stockage, applications) à la demande via Internet.

### ☁️ Modèles de Service (Cloud Service Models)

| Modèle | Signification | Description |
| :--- | :--- | :--- |
| **IaaS** | Infrastructure as a Service | Fournit à la demande des ressources d’infrastructure (machines virtuelles, stockage, réseau, etc.). Le client gère l'OS et les applications. |
| **PaaS** | Platform as a Service | Offre un environnement complet (OS, bases de données, outils de développement) pour développer et déployer des applications sans gérer l’infrastructure. |
| **SaaS** | Software as a Service | Propose des applications complètes accessibles en ligne, gérées et maintenues par le fournisseur (ex. messagerie, CRM). |

### 🌍 Types de Déploiement

* **Cloud public** : Ressources mutualisées hébergées chez un prestataire (Google Cloud, AWS, Azure). L’entreprise partage l’infrastructure, ce qui réduit les coûts et offre de la **scalabilité**.
* **Cloud privé** : Déploiement réservé à une seule organisation (sur site ou en hébergement dédié). Il offre plus de **contrôle et de sécurité** au prix d’un coût plus élevé et d’une évolutivité limitée.
* **Cloud hybride** : Combinaison d’environnements privés et publics, permettant de choisir le modèle le mieux adapté à chaque charge de travail.

Une vaste majorité d’entreprises (environ 90 %) adopte aujourd’hui une approche **multicloud ou hybride**.

### Avantages du Cloud
* **Évolutivité et agilité** : Augmenter ou réduire rapidement les ressources selon les besoins sans investissement initial massif.
* **Réduction des coûts** : Le modèle **pay-as-you-go** (payer à l'usage) permet de ne payer que ce qui est consommé.
* **Collaboration et accessibilité** : Les données sont disponibles partout via Internet.
* **Sécurité et résilience** : Les fournisseurs investissent dans des mécanismes de sécurité avancés, des solutions de sauvegarde et de reprise après sinistre intégrées.

### Défis et Limites
* **Dépendance à Internet** : Sans connexion fiable, l’accès aux services cloud est impossible.
* **Risque de panne fournisseur** : Des interruptions peuvent survenir, coupant l’accès aux ressources.
* **Verrouillage (lock-in)** : Migrer des applications d’un fournisseur à un autre peut être complexe.
* **Contrôle et conformité** : L’entreprise a moins de visibilité sur l’infrastructure sous-jacente (nécessité de respecter les normes comme le **RGPD**).
* **Intégration** : Combiner le cloud avec des systèmes existants (**legacy**) peut être complexe.


## VPC / VNet (Virtual Private Cloud / Virtual Network)

Un **VPC (Virtual Private Cloud)** ou **VNet (Virtual Network)** est un **réseau privé virtuel isolé** dans le cloud public. C’est l’équivalent d’un datacenter privé émulé dans le nuage.

* **Exemples** : Amazon VPC (AWS), Réseaux Virtuels (Azure).
* **Rôle** : Il permet à l’administrateur de créer des sous-réseaux isolés et de contrôler précisément les règles de routage et de sécurité dans son espace cloud.
* **Cas d’utilisation** : On utilise un VPC pour **segmenter et sécuriser** les ressources cloud. Par exemple, isoler une base de données critique dans un **sous-réseau privé protégé**, tout en hébergeant un serveur web dans un sous-réseau public. Il permet de relier de façon sécurisée un cloud public à un réseau privé d’entreprise via VPN.


## Load Balancers (Répartiteurs de charge)

Un **load balancer (équilibreur de charge)** est un dispositif qui **répartit le trafic réseau** sur plusieurs serveurs afin d’optimiser l’utilisation des ressources et de maintenir des performances élevées. Il agit comme intermédiaire entre les clients et les serveurs, routant chaque requête entrante vers le serveur le plus approprié.

* **But** : **Optimiser l'utilisation**, garantir la **haute disponibilité** et la **tolérance aux pannes**.

### Familles d’Équilibreurs
| Type | Couche OSI | Décision de Routage Basée sur... | Rôle |
| :--- | :--- | :--- | :--- |
| **Couche 4** | Transport | Adresses IP et ports TCP/UDP | Très rapide, adapté aux trafics non chiffrés. |
| **Couche 7** | Application | En-têtes HTTP (URL, cookies, etc.) | Plus flexible (terminaison TLS, routage géographique), mais plus gourmand en calcul. |

### Cas d’usage
* Gérer les **pics de trafic** et garantir la haute disponibilité devant des fermes de serveurs web ou d’applications.
* Effectuer des **« health checks »** (contrôles de santé) réguliers sur les serveurs pour retirer du pool ceux qui ne répondent plus.

## Sécurité de base : CIA, politiques d’accès, segmentation

### Triade CIA
Les principes fondamentaux de la sécurité de l’information reposent sur la triade **Confidentialité – Intégrité – Disponibilité (CIA)** :
* **Confidentialité** : Protéger les données contre tout accès non autorisé (ex. moindre privilège, chiffrement).
* **Intégrité** : Garantir que l’information reste exacte et inaltérée (via des contrôles d’intégrité).
* **Disponibilité** : Assurer que les ressources et données sont accessibles aux utilisateurs légitimes en permanence (redondance, sauvegardes).

### Politiques d’Accès
* Mise en place de mécanismes d’**authentification et d’autorisation** (authentification multifacteur, **RBAC** - Role-Based Access Control).
* L’idée est de ne donner aux utilisateurs que les permissions nécessaires à leur activité (**principe du moindre privilège**).

### Segmentation
* Consiste à **diviser le réseau en sous-réseaux isolés** (VLANs, DMZ), chacun avec ses propres règles de sécurité.
* Cette stratégie **limite la propagation d’une attaque** : un intrus pénétrant un segment ne peut pas atteindre automatiquement les autres.

## TLS (Transport Layer Security)

Le protocole **TLS** (évolution de SSL) est le standard de **sécurisation des communications** sur Internet. Il assure la **confidentialité et l’intégrité** des données en transit.

* **Mécanisme** : Chiffrement des échanges entre client et serveur via des **certificats numériques (X.509)** et un mécanisme de **clef publique/privée**.
* **Processus** : Le serveur présente un certificat pour s'**authentifier**. Client et serveur négocient ensuite des **clés symétriques** pour chiffrer la session.
* **Rôle Clé** : Il permet de naviguer en **HTTPS (HTTP sur TLS)** et de sécuriser les sessions VPN ou les canaux de messagerie. Les versions récentes (**TLS 1.2, TLS 1.3**) sont recommandées.


## Pare-feu

Un **pare-feu (firewall)** est une **barrière de protection** qui contrôle le trafic entre zones de confiance et zones externes. Il filtre le trafic selon des règles pré-définies (adresse IP, port, protocole).

### Types de Pare-feu
| Type | Couche OSI | Rôle |
| :--- | :--- | :--- |
| **Filtrage réseau** | Couche 3/4 | Inspecte selon les IP et ports. Peut être *stateless* ou *stateful* (avec suivi des connexions). |
| **Pare-feu applicatif (WAF)** | Couche 7 | Analyse le **contenu des requêtes** (HTTP/HTTPS) pour bloquer des attaques spécifiques au web (injections SQL, XSS). |
| **Matériel vs Logiciel** | Différents | Peut être un équipement physique dédié ou un logiciel installé sur une machine. |

### Configuration
* Les règles sont définies du plus précis au plus générique.
* La règle par défaut **« Refuser tout le reste (deny-all) »** est courante : elle interdit tout trafic qui n’est pas explicitement permis.


## IDS (Système de détection d’intrusion)

Un **IDS (Intrusion Detection System)** est une sonde de surveillance qui **analyse le trafic** ou les journaux des systèmes pour détecter des comportements anormaux ou malveillants, en s'appuyant sur des **signatures d’attaque**.

### Familles d’IDS
| Type | Emplacement | Rôle |
| :--- | :--- | :--- |
| **NIDS** | Sur le réseau | Surveille le trafic entre les machines (scans de ports, tentatives d'exploitation). |
| **HIDS** | Sur chaque hôte | Surveille les logs système, l’intégrité des fichiers et l’activité des applications sur la machine. |

### IDS vs IPS
* Un **IDS** se contente généralement d'**alerter** l’administrateur d’une attaque en cours.
* Un **IPS (Intrusion Prevention System)** est un IDS évolué qui peut, en plus, **réagir automatiquement en bloquant** ou en modifiant le trafic malveillant détecté.

### Exemples d’outils
* **Snort** : IDS/IPS open source très répandu.
* **Suricata** : IDS/IPS open source multi-thread, capable de scanner de hauts débits.
* **Autres** : Zeek, OSSEC.


Avez-vous besoin d'une explication plus détaillée sur la différence entre les équilibreurs de charge de couche 4 et de couche 7 ?
