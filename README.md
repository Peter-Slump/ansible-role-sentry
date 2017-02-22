# Ansible role Sentry

Version: 0.0.1

Supported OS: Ubuntu

Ansible role Sentry

- Configures Monit monitoring
- Uses PostgreSQL DB.
- Uses Redis

## Role variables
```
sentry_user: sentry
sentry_group: sentry
sentry_home: "/home/{{ sentry_user }}"

sentry_hostname: sentry.example.com

sentry_virtualenv_name: sentry
sentry_virtualenv_path: "{{ sentry_home }}/.virtualenv/{{ sentry_virtualenv_name }}"

sentry_database_name: sentry
sentry_database_user: sentry
sentry_database_password: ChangeMe
sentry_database_host: 127.0.0.1
sentry_database_port: 5432

sentry_secret_key: ChangeMeIAmInsecure

sentry_superuser_username: admin

sentry_port: 9004
sentry_listen_address: 0.0.1.0

sentry_use_letsencrypt: False
sentry_use_self_signed_ssl: False
```

## Example
```
- hosts: all
  roles:
   - role: sentry
     sentry_hostname: sentry.example.com
```
