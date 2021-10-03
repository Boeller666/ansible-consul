# Ansible Role Consul

This role installs [Hashicorp Consul](https://www.consul.io/).

## Requirements

- Version of the ansible for installation: >=2.8
- Supported OS:
  - Ubuntu
    - 18.04
    - 20.04

## Role Variables

- defaults:
  - `CONSUL_VERSION` \
    Version to install. Defualt: `1.8.0`
  - `CONSUL_FILENAME` \
    Filename to use for download. Default: `consul_{{ CONSUL_VERSION }}_linux_amd64.zip`
  - `CONSUL_DOWNLOAD_URL` \
    Consul download URL. Default: `https://releases.hashicorp.com/consul/{{ CONSUL_VERSION }}/{{ CONSUL_FILENAME }}`
  - `CONSUL_CHECKSUM_URL` \
    URL for the checksum file. Default: `https://releases.hashicorp.com/consul/{{ CONSUL_VERSION }}/consul_{{ CONSUL_VERSION }}_SHA256SUMS`

## Example Playbook

```yaml
- name: Converge
  hosts: consul
  roles:
    - role: ansible-consul
```

## License

BSD

## Author Information

- René Gärtner
