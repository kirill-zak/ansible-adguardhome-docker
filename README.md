adguardhome_docker
=========

AdguardHome in a Docker container for Ubuntu

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
