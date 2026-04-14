<!--
N.B. : Ce README a été généré automatiquement par https://github.com/YunoHost/apps/tree/main/tools/readme_generator
Il ne doit PAS être édité à la main.
-->

# LibreDesk pour YunoHost

[![Niveau d'intégration](https://dash.yunohost.org/integration/libredesk.svg)](https://dash.yunohost.org/appci/app/libredesk) ![Statut du fonctionnement](https://ci-apps.yunohost.org/ci/badges/libredesk.status.svg) ![Statut de maintenance](https://ci-apps.yunohost.org/ci/badges/libredesk.maintain.svg)<br>
[![Installer LibreDesk avec YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=libredesk)

*[Read this readme in English.](./README.md)*

> *Ce paquet vous permet d'installer LibreDesk rapidement et simplement sur un serveur YunoHost.
Si vous n'avez pas YunoHost, consultez [le guide](https://doc.yunohost.org/admin/get_started/install_on/) pour apprendre comment l'installer.*

## Vue d'ensemble

LibreDesk est un helpdesk client moderne, open source et auto-hébergé. Il se présente sous la forme d'un **binaire unique** s'appuyant sur PostgreSQL et Redis — sans Node, PHP ni Ruby. Le frontend est une application Vue 3 mono-page servie directement par le binaire.

### Fonctionnalités

- **Boîtes de réception partagées** – gérez support@, billing@, sales@ et plus depuis un seul endroit
- **Permissions granulaires** – contrôlez précisément ce que chaque agent ou équipe peut voir et faire
- **Automatisation intelligente** – taguez, assignez et routez automatiquement les conversations
- **Suivi des SLA** – définissez des objectifs de temps de réponse et recevez des alertes de dépassement
- **Enquêtes CSAT** – mesurez automatiquement la satisfaction client
- **Macros** – réponses types en un clic pouvant aussi modifier les tags ou le statut
- **Mises à jour en temps réel** – file d'attente live via WebSockets
- **AI-Assist** – reformulez les réponses pour le ton, la clarté ou le professionnalisme
- **Webhooks & API** – intégrez vos CRMs, outils analytiques ou workflows personnalisés

**Version incluse :** 0.11.0-beta~ynh1

**Démo :** <https://demo.libredesk.io>

## Captures d'écran

![Capture d'écran de LibreDesk](./doc/screenshots/screenshot.png)

## Avertissements / informations importantes

### Domaine dédié requis

LibreDesk **doit** être installé sur son propre domaine ou sous-domaine (ex. `helpdesk.example.com`). L'installation sous un sous-chemin (ex. `example.com/libredesk`) n'est **pas supportée** car le routeur SPA intégré de LibreDesk doit gérer l'intégralité de l'espace URL.

### Pas de LDAP / SSO

LibreDesk ne s'intègre pas au portail SSO ni à l'annuaire LDAP de YunoHost. Chaque compte utilisateur LibreDesk doit être créé manuellement dans LibreDesk. Le compte administrateur initial utilise le nom d'utilisateur **System** ; définissez son mot de passe lors de l'assistant d'installation YunoHost.

### Configuration initiale après l'installation

1. Ouvrez votre navigateur et accédez à votre domaine.
2. Connectez-vous avec l'identifiant `System` et le mot de passe choisi pendant l'installation.
3. Allez dans **Paramètres → Général** pour configurer le nom du site, le logo et le fuseau horaire.
4. Créez au moins une **Boîte de réception** (Paramètres → Boîtes de réception) pour commencer à recevoir des conversations.
5. Invitez vos agents de support (Paramètres → Agents).

### Architectures supportées

Seules les architectures **amd64** et **arm64** sont supportées. Il n'existe pas de builds 32 bits en amont.

## Documentations et ressources

- Site officiel de l'app : <https://libredesk.io>
- Documentation officielle : <https://docs.libredesk.io>
- Dépôt de code officiel de l'app : <https://github.com/abhinavxd/libredesk>
- YunoHost Store : <https://apps.yunohost.org/app/libredesk>
- Signaler un bug : <https://github.com/verzog/libredesk_ynh/issues>

## Informations pour les développeurs

Merci de faire vos pull requests sur la [branche testing](https://github.com/verzog/libredesk_ynh/tree/testing).

Pour essayer la branche testing, procédez comme suit :

```bash
sudo yunohost app install https://github.com/verzog/libredesk_ynh/tree/testing --debug
ou
sudo yunohost app upgrade libredesk -u https://github.com/verzog/libredesk_ynh/tree/testing --debug
```

**Plus d'infos sur le packaging d'applications :** <https://doc.yunohost.org/dev/packaging/>
