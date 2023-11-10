# AlmaLinux Container image for Ansible

Systemd AlmaLinux container images for testing roles with molecule.
Support versions:

- '9'

## Available images

Images are built weekly via Github Actions and can be downloaded from the Github Package Repository.

These tags are available. They are updated once a week or on merges to main.

- 'ghcr.io/bpadair32/alma-systemd:9'

## Usage

- Install Docker
- Run the container via Docker:

```bash
docker run -itd --privileged ghcr.io/bpadair32/alma-systemd:9
```

## Authors

Built and maintained by Brad Adair, brad@adair.tech.
Inspired by GeerlingGuy, https://github.com/geerlingguy.
