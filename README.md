# TareaAnsibleDHCP-DNS-InfraestructuraIII

# ansible-rocky9-dns-dhcp

Playbook de Ansible idempotente para instalar y configurar **DNS (BIND/named)**
y **DHCP (dhcpd/ISC)** en **Rocky Linux 9**, con zonas forward/reverse,
firewalld, notas de SELinux y validaciones automáticas (`named-checkconf`,
`named-checkzone`, `dhcpd -t`).

## Requisitos

- Rocky Linux 9 en los hosts objetivo
- Ansible >= 2.14 en el nodo de control
- Colección `ansible.posix` (usada por el módulo `firewalld`):
```bash
  ansible-galaxy collection install ansible.posix
```
- Acceso SSH + `become` (sudo) al host objetivo
- Conectividad de red hacia el/los host(s) definidos en `inventory/hosts.ini`

