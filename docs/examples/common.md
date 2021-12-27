<!-- Space: AnsibleRoleCertbot -->
<!-- Parent: Project -->
<!-- Title: Project Examples -->

<!-- Label: Examples -->
<!-- Include: docs/disclaimer.md -->
<!-- Include: ac:toc -->

## basic

To run this playbook with default settings, create a basic playbook like this:

```{.yaml}
- hosts: servers
  roles:
    - hadenlabs.certbot

  vars:
    certbot_create_if_missing: false
    certbot_create_method: standalone
    certbot_admin_email: luis@handelabs.com
    certbot_create_standalone_stop_services:
    - nginx
    certbot_vhosts:
        - {servername: "abcyourdomain.com", documentroot: "/var/www/abcyourdomain.com"}
        - {servername: "abcyourdomain1.com", documentroot: "/var/www/abcyourdomain1.com"}
```
