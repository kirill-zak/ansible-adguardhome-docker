adguardhome_docker
=========

Setup and run AdguardHome in a Docker container

## Support distributive

* AlmaLinux 9
* CentOS 8
* Debian 10 (Buster)
* Debian 11 (Bullseye)
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
