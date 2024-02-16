adguardhome_docker
=========

Setup and run AdguardHome in a Docker container

## Support distributive

* AlmaLinux 9
* Alpine Linux 3.16.x (`3.16.0`, `3.16.1`, `3.16.2`, `3.16.3`, `3.16.4`, `3.16.5`, `3.16.6`, `3.16.7`, `3.16.8`, `3.16.9`)
* Alpine Linux 3.17.x (`3.17.0`, `3.17.1`, `3.17.2`, `3.17.3`, `3.17.4`, `3.17.5`, `3.17.6`, `3.17.7`)
* Alpine Linux 3.18.x (`3.18.0`, `3.18.2`, `3.18.3`, `3.18.4`, `3.18.5`, `3.18.6`)
* Alpine Linux 3.19.x (`3.19.0`, `3.19.1`)
* CentOS 8
* Debian 10 (Buster)
* Debian 11 (Bullseye)
* Fedora Linux 35
* Fedora Linux 36
* Fedora Linux 37
* Fedora Linux 38
* Rocky Linux 9
* Ubuntu 18.04 (Bionic Beaver)
* Ubuntu 20.04 (Focal Fossa)
* Ubuntu 22.04 (Jammy Jellyfish)

## Requirements

Docker engine

## Role Variables

- `adguardhome_docker_admin_panel_port`: Port of admin panel. Default value `8080`.
- `adguardhome_docker_container_name`: Name of container. Default value `adguardhome`.
- `adguardhome_docker_network`: Name of docker network. Default value `adguardhome`.
- `adguardhome_docker_tag`: Tag found at # https://hub.docker.com/r/adguard/adguardhome/tags

## Dependencies

- Docker

## Example Playbook

```yaml
    - name: Install AdguardHome
      hosts: adguardhome
      become: true
      vars:
        adguardhome_docker_admin_panel_port: 8080
      roles:
        - role: kirill_zak.ansible_docker
        - role: kirill_zak.adguardhome_docker
```

## License

GPL-2.0

## Author Information

https://kirill-zak.ru
