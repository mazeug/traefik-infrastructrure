# Architecture

## Overview

Traefik runs centrally on the Mini-PC.

It receives HTTP and HTTPS traffic and routes requests to services
running in different environments.

## Environments

### Local Docker

Traefik watches the local Docker daemon.

### External Docker Swarm

Traefik connects to the Docker Swarm manager API and discovers
services deployed in the Swarm.

### External Kubernetes

Traefik connects to the Kubernetes API server and discovers
Kubernetes routing resources.

### File Provider

Common infrastructure configuration is maintained in Git using
the Traefik file provider.

## Source of Truth

Git is the source of truth for:

- Docker Compose
- Traefik static configuration
- Traefik dynamic configuration
- Middleware definitions
- TLS configuration
- Deployment scripts
- Documentation

Runtime data is not stored in Git.

## Persistent Data

Persistent Traefik data is stored on NFS.

Example:

/mnt/nfs/traefik/

This includes Let's Encrypt ACME state.
