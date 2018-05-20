dc-redmine
=========

Install redmine (based on Redmine)

Requirements
------------

none

Role Variables
--------------

```
# common settings
dc_redmine_timezone: Asia/Tokyo

# redmine settings
dc_redmine_redmine_port: 10083
dc_redmine_redmine_https: false
dc_redmine_redmine_relative_url_root: 
dc_redmine_redmine_secret_token:
dc_redmine_redmine_sudo_mode_enabled: false
dc_redmine_redmine_sudo_mode_timeout: 15
dc_redmine_redmine_concurrent_uploads: 2
dc_redmine_redmine_backup_schedule:
dc_redmine_redmine_backup_expiry:
dc_redmine_redmine_backup_time:

# smtp settings
dc_redmine_smtp_enabled: false
dc_redmine_smtp_method: smtp
dc_redmine_smtp_domain: www.example.com
dc_redmine_smtp_host: smtp.gmail.com
dc_redmine_smtp_port: 587
dc_redmine_smtp_user: mailer@example.com
dc_redmine_smtp_pass: password
dc_redmine_smtp_starttls: true
dc_redmine_smtp_authentication: :login

# imap settings
dc_redmine_imap_enabled: false
dc_redmine_imap_host: imap.gmail.com
dc_redmine_imap_port: 993
dc_redmine_imap_user: mailer@example.com
dc_redmine_imap_pass: password
dc_redmine_imap_ssl: true
dc_redmine_imap_interval: 30

# database settings
dc_redmine_db_adapter: postgresql
dc_redmine_db_host: postgresql
dc_redmine_db_port: 5432
dc_redmine_db_user: redmine
dc_redmine_db_pass: password
dc_redmine_db_name: redmine_production

# reverse proxy settings
dc_redmine_domains: 'redmine.example.com -> http://redmine'
dc_redmine_stage: production
```

Dependencies
------------

[douhashi/ansible-role-docker-compose](https://github.com/douhashi/ansible-role-docker-compose)


Example Playbook
----------------

```
- hosts: servers
  roles:
    - dc-redmine
```

License
-------

MIT

Author Information
------------------

[Sho DOUHASHI](https://github.com/douhashi)

