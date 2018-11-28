

## Recommendation de l'[ANSSI](https://www.ssi.gouv.fr/administration/bonnes-pratiques/)

Ci dessous, la liste des recommandations de l'ANSII concernant les "Administrations" vis à vis des [principales menaces](https://www.ssi.gouv.fr/administration/principales-menaces/). Pour chaque recommandation, nous présentons quand c'est appliquable au projet Regovar ce qui a été fait.

### Cryptographie

| Recomandation | Appliquable | Commentaire |
| ------------- | ----------- | ----------- |
| [Recommandations de sécurité relatives à TLS](https://www.ssi.gouv.fr/administration/guide/recommandations-de-securite-relatives-a-tls/) |  OUI | 
| [CRYPTO : LE WEBDOC’](https://www.ssi.gouv.fr/administration/guide/crypto-le-webdoc/) | 

### Poste de travail et serveurs

| Recomandation | Appliquable | Commentaire |
| ------------- | ----------- | ----------- |



### Lisaisons sans fil et mobilité

| Recomandation | Appliquable | Commentaire |
| ------------- | ----------- | ----------- |


### Réseaux

| Recomandation | Appliquable | Commentaire |
| ------------- | ----------- | ----------- |


### Applications WEB

| Recomandation | Appliquable | Commentaire |
| ------------- | ----------- | ----------- |

### Externalisation

| Recomandation | Appliquable | Commentaire |
| ------------- | ----------- | ----------- |


### Dispositifs de vidéoprojection

Si Regovar pourra être utilisé et présenté lors de réunion, il n'a pas vocation à gérer lui-même la vidéoprojection. Ces recommandations sont assurer par les DSI des CHU et ne s'appliquent donc pas au projet Regovar.

| Recomandation | Appliquable | Commentaire |
| ------------- | ----------- | ----------- |
| [Sécuriser vos dispositifs de vidéoprojection](https://www.ssi.gouv.fr/administration/guide/recommandations-de-securite-pour-la-mise-en-oeuvre-de-dispositifs-de-videoprotection/) |NON | |

### Système industriel

| Recomandation | Appliquable | Commentaire |
| ------------- | ----------- | ----------- |


### Technologies sans contact

| Recomandation | Appliquable | Commentaire |
| ------------- | ----------- | ----------- |



### Méthodologie

| Recomandation | Appliquable | Commentaire |
| ------------- | ----------- | ----------- |
| [Cartographie du système d'information](https://www.ssi.gouv.fr/administration/guide/cartographie-du-systeme-dinformation/) | OUI | Voir la section '[Architecture]()' de la documentation technique. |
| [Agilité et sécurité numériques](https://www.ssi.gouv.fr/administration/guide/agilite-et-securite-numeriques-methode-et-outils-a-lusage-des-equipes-projet/) | OUI | Lecture conseillé pour les architectes et développeurs du projet. 
TODO: mise en oeuvre ? |
| [Protection du potentiel scientifique et technique de la nation](https://www.ssi.gouv.fr/administration/guide/protection-du-potentiel-scientifique-et-technique-de-la-nation/) | NON |Le projet Regovar est libre et open-source. Il n'y a pas de brevet ni de secret technique à protéger. |
| [Intégrer la sécurité dans une démarche agile](https://www.ssi.gouv.fr/administration/guide/integrer-la-securite-numerique-dans-une-demarche-agile/) |  | A 
| [Recommandations et méthodologie pour le nettoyage d'une politique de filtrage réseau d'un pare-feu](https://www.ssi.gouv.fr/administration/guide/recommandations-et-methodologie-pour-le-nettoyage-dune-politique-de-filtrage-reseau-dun-pare-feu/) | OUI | Dans le cadre de l'installation stand-alone du serveur Regovar. |
| [Achat de produits de sécurité et de services de confiance qualifiés dans le cadre du RGS](https://www.ssi.gouv.fr/administration/guide/achat-de-produits-de-securite-et-de-services-de-confiance-qualifies-dans-le-cadre-du-rgs/) | NON | L'achat de matériel quand il a lieu doit passer par la DSI des CHUs, qui respecteront les procédures nécessaires. |
| [L'homologation de sécurité en neuf étapes simples](https://www.ssi.gouv.fr/administration/guide/lhomologation-de-securite-en-neuf-etapes-simples/) | OUI | TODO |
| [EBIOS - Expressions des besoins et identifications des objectifs de sécurité](https://www.ssi.gouv.fr/administration/guide/ebios-2010-expression-des-besoins-et-identification-des-objectifs-de-securite/) | NON | Obsolète depuis 2010. |
| [La défense en profondeur appliquée aux systèmes d'information](https://www.ssi.gouv.fr/administration/guide/la-defense-en-profondeur-appliquee-aux-systemes-dinformation/) | OUI | Lecture conseillé pour les architectes et développeurs du projet. TODO: |
| [Archivage électronique... comment le sécuriser](https://www.ssi.gouv.fr/administration/guide/archivage-electronique-comment-le-securiser/) | NON | L'archivage des données n'est pas assurée par Regovar, mais par les CHUs qui ont tous déjà mis en place ce qu'il faut pour ça. |
| [PSSI - Guide de l'élaboration de politiques de sécurité des systèmes d'information](https://www.ssi.gouv.fr/administration/guide/pssi-guide-delaboration-de-politiques-de-securite-des-systemes-dinformation/) | | TODO |
| [TDBSSI - Guide d'élaboration de tableaux de bord de sécurité des systèmes d'information](https://www.ssi.gouv.fr/administration/guide/tdbssi-guide-delaboration-de-tableaux-de-bord-de-securite-des-systemes-dinformation/) | | TODO |
| [Guide relatif à la maturité SSI](https://www.ssi.gouv.fr/administration/guide/guide-relatif-a-la-maturite-ssi/) | OUI | TODO. |
| [GISSIP - Guide d'intégration de la sécurité des systèmes d'informations dans les projets](https://www.ssi.gouv.fr/administration/guide/gissip-guide-dintegration-de-la-securite-des-systemes-dinformation-dans-les-projets/) | OUI | Lecture conseillé pour les architectes et développeurs du projet. TODO |




## Standards

Ci dessous, la liste des normes et des standards utilisé dans le projet Regovar

| Identifiant | Commentaire |
| ----------- | ----------- |
| [XML](https://www.w3.org/TR/2006/REC-xml11-20060816/) | Regovar privilégie JSON dans ses formats d'échange,  et éviter au max XML.


### A l'étude
Ci dessous la liste des RFC, à voir si on les appliques ou pas, et comment on s'y prend.
* [Textual Encodings of PKIX, PKCS, and CMS Structures](https://tools.ietf.org/html/rfc7468) : Quel algo de chiffrage / format utilisé pour les certificats et keystore ? <= ANSSI impose des choix en fonction du niveau de classification.
    * [X509](https://tools.ietf.org/html/rfc6818)
    * [X690](https://www.itu.int/rec/T-REC-X.690-201508-I/en)


[RFC793]	https://tools.ietf.org/html/rfc793
Transmission Control Protocol - Darpa Internet Program Protocol Specification.

[RFC2986]	https://tools.ietf.org/html/rfc2986
PKCS #10: Certification Request Syntax Specification Version 1.7

[RFC2315]	https://tools.ietf.org/html/rfc2315
PKCS #7: Cryptographic Message Syntax Version 1.5

[RFC3948]	https://tools.ietf.org/html/rfc3948	UDP Encapsulation of IPsec ESP Packets

[RFC3986]	https://tools.ietf.org/html/rfc3986
Uniform Resource Identifier (URI): Generic Syntax

[RFC4301]	https://tools.ietf.org/html/rfc4301	Security Architecture for the Internet Protocol

[RFC4303]	https://tools.ietf.org/html/rfc4303	IP Encapsulating Security Payload (ESP)

[RFC5246]	https://tools.ietf.org/html/rfc5246
The Transport Layer Security (TLS) Protocol Version 1.2

[RFC5280]	https://tools.ietf.org/html/rfc5280
Internet X.509 Public Key Infrastructure Certificate and Certificate Revocation List (CRL) Profile

[RFC5424]	https://tools.ietf.org/html/rfc5424
The Syslog Protocol

[RFC5425]	https://tools.ietf.org/html/rfc5425
Transport Layer Security (TLS) Transport Mapping for Syslog

[RFC5652]	https://tools.ietf.org/html/rfc5652
Cryptographic Message Syntax (CMS)

[RFC5905]	https://tools.ietf.org/html/rfc5905
Network Time Protocol Version 4: Protocol and Algorithms Specification

[RFC6020]	https://tools.ietf.org/html/rfc6020
YANG - A Data Modeling Language for the Network Configuration Protocol (NETCONF

[RFC6241]	https://tools.ietf.org/html/rfc6241
Network Configuration Protocol (NETCONF)

[RFC6991]	https://tools.ietf.org/html/rfc6991
Common YANG Data Types

[RFC6335]	https://tools.ietf.org/html/rfc6335
Internet Assigned Numbers Authority (IANA) Procedures for the Management of the Service Name and Transport Protocol Port Number Registry

[RFC4632]	https://tools.ietf.org/html/rfc4632
Classless Inter-domain Routing (CIDR): The Internet Address Assignment and Aggregation Plan

[RFC7296]	https://tools.ietf.org/html/rfc7296
Internet Key Exchange Protocol Version 2 (IKEv2)

[RFC7589]	https://tools.ietf.org/html/rfc7589	Using the NETCONF Protocol over Transport Layer Security (TLS) with Mutual X.509 Authentication	

[RFC8071]	https://tools.ietf.org/html/rfc8071
NETCONF Call Home and RESTCONF Call Home

[RFC8259]	https://tools.ietf.org/html/rfc8259
The JavaScript Object Notation (JSON) Data Interchange Format

[USB]	http://www.usb.org/developers/docs/
Universal Serial Bus Revision 3.1 Specification	07/2013	USB Implementers Forum
[ISO8802]	ISO/IEC 8802-3-2014	8802-3-2014 - ISO/IEC/IEEE International Standard for Ethernet

[IEEE802.3]	IEEE 802.3	802.3- IEEE Standard for Ethernet

[SFF8431]	SFF-8431	SFF Committee - SFF-8431 Specifications for Enhanced Small Form Factor Pluggable Module SFP+. Revision 4.1. 6th of July 2009.

 
 
 
 [RFC 791]	https://tools.ietf.org/html/rfc791
Internet Protocol
DARPA Internet Program Protocol Specification

[RFC 792]	https://tools.ietf.org/html/rfc792
Internet Control Message Protocol
DARPA Internet Program Protocol Specification

[RFC 826]	https://tools.ietf.org/html/rfc826
An Ethernet Address Resolution Protocol -- or -- Converting Network Protocol Addresses to 48.bit Ethernet Address for Transmission on Ethernet Hardware

[RFC 1191]	https://tools.ietf.org/html/rfc1191
Path MTU Discovery (PMTUd)

[RFC 1213]	https://tools.ietf.org/html/rfc1213
Management Information Base for Network Management of TCP/IP -based internets: MIB-II

[RFC 2131]	https://tools.ietf.org/html/rfc2131
Dynamic Host Configuration Protocol

[RFC 2328]	https://tools.ietf.org/html/rfc2328
OSPF Version 2

[RFC 2674]	https://tools.ietf.org/html/rfc2674
Definitions of Managed Objects for Bridges with Traffic Classes, Multicast Filtering and Virtual LAN Extensions (VLAN)

[RFC 3069]	https://tools.ietf.org/html/rfc3069
VLAN Aggregation for Efficient IP Address Allocation

[RFC 3195]	https://tools.ietf.org/html/rfc3195
Reliable Delivery for syslog

[RFC 3315]	https://tools.ietf.org/html/rfc3315
Dynamic Host Configuration Protocol for IPv6 (DHCPv6)

[RFC 3413]	https://tools.ietf.org/html/rfc3413
Simple Network Management Protocol (SNMP) Applications

[RFC 3414]	https://tools.ietf.org/html/rfc3414
User-based Security Model (USM) for version 3 of the Simple Network Management Protocol (SNMPv3)

[RFC 4293]	https://tools.ietf.org/html/rfc4293
Management Information Base (MIB) for the Internet Protocol (IP)

[RFC 4301]	https://tools.ietf.org/html/rfc4301
Security Architecture for the Internet Protocol

[RFC 4303]	https://tools.ietf.org/html/rfc4303
IP Encapsulating Security Payload (ESP)

[RFC 4807]	https://tools.ietf.org/html/rfc4807
IPsec Security Policy Database Configuration MIB

[RFC 4443]	https://tools.ietf.org/html/rfc4443
Internet Control Message Protocol (ICMPv6) for the Internet Protocol Version 6 (IPv6) Specification

[RFC 4861]	https://tools.ietf.org/html/rfc4861
Neighbor Discovery for IP version 6 (IPv6)

[RFC 5280]	https://tools.ietf.org/html/rfc5280
Internet X.509 Public Key Infrastructure Certificate and Certificate Revocation List (CRL) Profile

[RFC 5340]	https://tools.ietf.org/html/rfc5340
OSPF for IPv6

[RFC 5424]	https://tools.ietf.org/html/rfc5424
The SYSLOG Protocol

[RFC 5425]	https://tools.ietf.org/html/rfc5425
Transport Layer Security (TLS) Transport Mapping for Syslog

[RFC 5426]	https://tools.ietf.org/html/rfc5426
Transmission of Syslog Messages over UDP

[RFC 5591]	https://tools.ietf.org/html/rfc5591
Transport Security Model for the Simple Network Management Protocol (SNMP)

[RFC 6241]	https://tools.ietf.org/html/rfc6241
Network Configuration Protocol (NETCONF)

[RFC 6587]	https://tools.ietf.org/html/rfc6587
Transmission of Syslog Messages over TCP

[RFC 8200]	https://tools.ietf.org/html/rfc8200
Internet Protocol, Version 6 (IPv6) Specification

[RFC 8201]	https://tools.ietf.org/html/rfc8201
Path MTU Discovery for IP version 6

[ISO 8601]	ISO 8601
https://www.iso.org/fr/standard/40874.html
ISO 8601:2004: Éléments de données et formats d'échange -- Échange d'information -- Représentation de la date et de l'heure	ISO 8601:2004 

[ISO/IEC 9594-2]	https://www.iso.org/fr/standard/72551.html
ISO/IEC 9594-2:2017 : Interconnexion de systèmes ouverts (OSI) -- L'annuaire -- Partie 2: Les modèles

[ISO/IEC 9594-8]	https://www.iso.org/fr/standard/72557.html
ISO/IEC 9594-8:2017 : Interconnexion de systèmes ouverts (OSI) -- L'annuaire -- Partie 8: Cadre général des certificats de clé publique et d'attribut

[IANA]	IANA-IKEv2 	IANA Internet Key Exchange Version 2 (IKEv2) Parameters	01/2005
(MAJ : 04/2017)	IANA

[IEEE 802.1Q]	http://www.ieee802.org/1/pages/802.1Q.html
802.1Q - Virtual LANs	MAJ : 11/2014	IEEE

[IEEE 802.3]	http://www.ieee802.org/3/
IEEE 802.3 Ethernet Working Group	MAJ : 01/2018)	IEEE

[WCAG]	https://www.w3.org/TR/WCAG20/
Web Content Accessibility Guidelines (WCAG)	2.0	W3C

[DSP0243]	https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_2.1.1.pdf
Open Virtualization Format Specification	2.1.1 (08/2015)	DMTF



## COTS

Ci dessous, la liste des COTS utilisé dans le projet Regovar et livré dans le produit final. (Ne sont pas présent les outils utilisés uniquement pour le développement par exemple).

| COTS | Version | License | Description | Commentaire |
| ---- | ------- | ------- | ----------- | ----------- |

* docker
* postgreSQL

### Modules pythons

| COTS | Version | License | Description | Commentaire |
| ---- | ------- | ------- | ----------- | ----------- |

### Librairies javascripts

| COTS | Version | License | Description | Commentaire |
| ---- | ------- | ------- | ----------- | ----------- |


