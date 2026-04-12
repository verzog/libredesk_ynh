## Dedicated domain required

LibreDesk **must** be installed on its own domain or subdomain (e.g. `helpdesk.example.com`). Installing it under a sub-path (e.g. `example.com/libredesk`) is **not supported** because LibreDesk's built-in SPA router needs to own the entire URL space.

## No LDAP / SSO

LibreDesk does not integrate with YunoHost's SSO portal or LDAP directory. Each LibreDesk user account must be created manually inside LibreDesk. The initial admin account is named **System**; set its password during the YunoHost install wizard.

## First-time setup after install

After the package installs successfully:

1. Open your browser and navigate to your domain.
2. Log in with username `System` and the password you chose during installation.
3. Go to **Settings → General** to configure your site name, logo, and timezone.
4. Create at least one **Inbox** (Settings → Inboxes) to start receiving conversations.
5. Invite your support agents (Settings → Agents).

## Upgrading

Always take a database backup before upgrading:

```bash
sudo yunohost backup create --apps libredesk
```

Then upgrade as normal through the YunoHost web admin or:

```bash
sudo yunohost app upgrade libredesk
```

Database migrations run automatically during the upgrade.

## Supported architectures

Only **amd64** (standard 64-bit servers/desktops) and **arm64** (Raspberry Pi 4+, etc.) are supported. There are no 32-bit builds available upstream.
