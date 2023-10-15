Role Name
=========

install vaultwarden with caddy

Requirements
------------


Role Variables
--------------
| defaults variable | description |default value|mandatory|
|-------------------|-------------|-------------|---------|
|app_user|user for the install directory| pihole|no|
|docker_home|base install directory| /opt/docker|no|
|docker_dirs|list of installation sub-directory||no|
|vaultwarden_env| template name| vaultwarden.env|no|
|timezone|Timezone| Europe/Vienna|no|
|smtp_port|smtp server port| 587|no|
|vault_smtp_server|smtp server|no default|yes|
|vault_smtp_login|smtp auth login|no default|yes|
|vault_smtp_password|smtp auth password|no default|yes|
|vault_mail_from_vaultwarden|from address|no default|yes|

|vwbk_BACKUP_FILE_SUFFIX|date format| '%Y%m%d'|no|
|vwbk_BACKUP_KEEP_DAYS|number of days to keep| 10|no|
|vwbk_CRON|cron config| '0 1 * * *'|no|
|vw_image|vw image name| vaultwarden/server:1.29.2|no|
|vw_data_folder|data folder| data|no|
|vw_rocket_address|| 0.0.0.0|no|
|vw_rocket_port|| 8001|no|
|vault_vw_admin_token||no default|yes|
|vw_backup_image|vault warden backup image| ttionya/vaultwarden-backup|no|
|vault_ZIP_PASSWORD||no default|yes|
|caddy_image|| juharov/caddy-duckdns-cloudflare|no|
|vault_vw_caddy_domain4||no default|yes|
|vault_vw_duckdns_token||no default|yes|


Dependencies
------------

* caddy_image: juharov/caddy-duckdns-cloudflare:latest

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-vaultwarden-caddy }

License
-------

This project is licensed under the Attribution-NonCommercial-ShareAlike 4.0 International License - see the [LICENSE.md](LICENSE.md) file for details

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
