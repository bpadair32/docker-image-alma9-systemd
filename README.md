# AlmaLinux Container image for Ansible Testing

[![Build](https://github.com/bpadair32/docker-image-alma9-systemd/actions/workflows/build.yml/badge.svg)](https://github.com/bpadair32/docker-image-alma9-systemd/actions/workflows/build.yml)

Systemd AlmaLinux container images for testing roles and playbooks with molecule.

## Available images

Images are built weekly via Github Actions and can be downloaded from the Github Package Repository.

These tags are available. They are updated once a week or on merges to main.

- 'ghcr.io/bpadair32/alma-systemd:latest'

## Usage

- [Install Docker](https://docs.docker.com/engine/installation/).
- Pull the image from GitHub Container Repository: `docker pull ghcr.io/bpadair32/docker-image-alma9-systemd:latest` 
- Run the container via Docker:

```bash
docker run -- detach --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:rw --cgroupns=host ghcr.io/bpadair32/docker-image-alma9-systemd:latest --volume='pwd':/etc/ansible/roles/role_to_test:ro
```
- Run ansible commands inside the container:
  a. `docker exec --tty [container_id] env TERM=xterm ansible --version`
  b. `docker exec --tty [container_id] env TERM=xterm ansible-playbook /path-to/playbook.yml --syntax-check` 

## Authors

Built and maintained by Brad Adair, brad@adair.tech.
Inspired by GeerlingGuy, https://github.com/geerlingguy.
