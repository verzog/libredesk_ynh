# LibreDesk pour YunoHost

[![Niveau d'intégration](https://dash.yunohost.org/integration/libredesk.svg)](https://dash.yunohost.org/appci/app/libredesk)
[![Installer LibreDesk avec YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=libredesk)

*[Read this readme in English.](./README.md)*

> *Ce paquet vous permet d'installer LibreDesk rapidement et simplement sur un serveur YunoHost.
> Si vous n'avez pas YunoHost, consultez [le guide](https://doc.yunohost.org/admin/get_started/install_on/) pour apprendre comment l'installer.*

## Vue d'ensemble

LibreDesk est un helpdesk client moderne, open source et auto-hébergé. Il se présente sous la forme d'un **binaire unique** s'appuyant sur PostgreSQL et Redis.

### Fonctionnalités

- **Boîtes de réception partagées** – Connectez support@, billing@, sales@ et plus encore.
- **Permissions granulaires** – Créez des rôles personnalisés pour les équipes et les agents.
- **Automatisation intelligente** – Taguez, assignez et routez les conversations automatiquement.
- **Enquêtes CSAT** – Mesurez la satisfaction client.
- **Macros** – Enregistrez des réponses types et appliquez-les en un clic.
- **Gestion des SLA** – Définissez des objectifs de temps de réponse.
- **Mises à jour en temps réel** – Via WebSockets.
- **AI-Assist** – Reformulez les réponses des agents.
- **Webhooks** – Intégrez vos CRMs et systèmes externes.

**Version incluse :** 0.11.0-beta~ynh1

**Démo :** <https://demo.libredesk.io>

## Avertissements / informations importantes

- LibreDesk **nécessite un domaine dédié** (ou sous-domaine). Il ne peut pas fonctionner sous un sous-chemin comme `exemple.com/libredesk`.
- LDAP / SSO YunoHost ne sont **pas supportés**. Les utilisateurs se connectent avec les identifiants propres à LibreDesk. Le compte admin initial s'appelle `System` et utilise le mot de passe choisi lors de l'installation.
- Seules les architectures `amd64` et `arm64` sont supportées.

## Documentation et ressources

- Site officiel : <https://libredesk.io>
- Documentation officielle : <https://docs.libredesk.io>
- Dépôt de code upstream : <https://github.com/abhinavxd/libredesk>
- Signaler un bug dans ce paquet : <https://github.com/YunoHost-Apps/libredesk_ynh/issues>
