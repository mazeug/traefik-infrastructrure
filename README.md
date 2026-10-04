# Traefik Infrastructure

Central Traefik reverse proxy running on the Docker host of the Mini-PC.

## Managed environments

- Local Docker
- External Docker Swarm
- External Kubernetes cluster

## Repository principles

- Git is the source of truth.
- No secrets are stored in Git.
- Persistent runtime data is stored on external NFS.
- Traefik runs as a Docker container on the Mini-PC.
- Portainer may be used for inspection and operational tasks.

## Architecture

See:

- docs/architecture.md
- docs/networking.md
- docs/installation.md
