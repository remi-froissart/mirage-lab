# Mirage Lab

Homelab d’administration **systèmes, réseaux, virtualisation et sécurité**, conçu pour mettre en pratique des technologies utilisées en environnement professionnel.

Le projet me permet de construire, administrer, sécuriser et documenter une infrastructure complète en reproduisant différents scénarios d’entreprise.

## 🏗️ Architecture

L’environnement repose actuellement sur :

* **VMware Workstation Pro** comme hyperviseur hôte
* **Proxmox VE** pour la virtualisation
* **OPNsense** pour le routage, le pare-feu et la segmentation réseau
* **ZFS** pour le stockage des machines virtuelles
* **Docker** pour l’hébergement de services
* **Traefik** comme reverse proxy
* **Cloudflare Tunnel** pour la publication sécurisée de services

### Segmentation réseau

| Réseau | Sous-réseau    | Usage                            |
| ------ | -------------- | -------------------------------- |
| LAN    | `10.0.10.0/24` | Postes clients et administration |
| DMZ    | `10.0.20.0/24` | Services exposés                 |
| SRV    | `10.0.30.0/24` | Serveurs internes                |

## 🔐 Sécurité

Plusieurs mécanismes sont mis en œuvre afin d'appliquer une logique de défense en profondeur :

* segmentation réseau par zones et interfaces
* filtrage inter-réseaux avec OPNsense
* DNSSEC
* DNS over TLS
* reverse proxy
* Cloudflare Tunnel
* aucun port entrant directement exposé
* règles WAF et rate limiting
* durcissement du serveur et des conteneurs Docker
* en-têtes de sécurité HTTP
* mises à jour automatiques des systèmes

## 🐳 Services

L'infrastructure contient actuellement notamment :

* Traefik
* Docker
* Cloudflared
* serveur web de documentation
* DNS Unbound avec DNSSEC et DNS over TLS
* pare-feu et routage OPNsense
* DHCP Kea

### En cours d'intégration

* développement d'une application avec **Python**
* mise en place et administration d'une base de données **PostgreSQL**

D'autres services seront ajoutés au fur et à mesure de l'évolution du lab.

## 🎯 Objectifs

Ce projet me permet notamment de travailler :

* l'administration Linux
* la virtualisation avec Proxmox VE
* le stockage ZFS
* les réseaux TCP/IP
* le routage et les pare-feu
* la segmentation réseau
* OPNsense
* DHCP et DNS
* DNSSEC et DNS over TLS
* Docker et les conteneurs
* les reverse proxies avec Traefik
* la sécurisation des accès SSH
* le durcissement des serveurs et conteneurs
* la publication sécurisée de services
* Cloudflare Tunnel
* WAF et sécurité HTTP
* l'automatisation des mises à jour système

### En cours d'apprentissage et d'intégration

* Python
* PostgreSQL
* interaction entre une application et une base de données

## 📚 Documentation

La documentation détaillée du projet est disponible sur :

**https://docs.mirage-lab.cloud**

## 🚧 État du projet

Mirage Lab est un environnement en évolution continue. De nouvelles briques sont régulièrement ajoutées afin d'expérimenter différentes architectures et problématiques d'administration système et réseau.

---

**Rémi Froissart**  
Administrateur systèmes & réseaux
