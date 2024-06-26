# Ansible-Role: acr-ansible-samba-share

AIT-CyberRange: Installs and configures basic samba share.


## Requirements

- Debian or Ubuntu 

## Role Variables

```yaml
samba_workgroup: 'WORKGROUP'
samba_server_string: 'Fileserver %m'
samba_log_size: 5000
samba_log_level: 0
samba_interfaces: []
samba_security: 'user'
samba_passdb_backend: 'tdbsam'
samba_map_to_guest: 'never'
samba_load_printers: false
samba_printer_type: 'cups'
samba_cups_server: 'localhost:631'
samba_load_homes: false
samba_create_varwww_symlinks: false
samba_shares_root: '/srv/shares'
samba_shares: []
samba_users: []

samba_wins_support: 'yes'
samba_local_master: 'yes'
samba_domain_master: 'yes'
samba_preferred_master: 'yes'
samba_mitigate_cve_2017_7494: true

samba_configuration_dir: /etc/samba
samba_configuration: "{{ samba_configuration_dir }}/smb.conf"
samba_username_map_file: "{{ samba_configuration_dir }}/smbusers"
```

## Example Playbook

```yaml
- hosts: localhost
  roles:
    - acr-ansible-samba-share
```

## License

GPL-3.0

## Author

- Lenhard Reuter