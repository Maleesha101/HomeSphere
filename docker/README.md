# Docker Services

Planned service packages:

- vendor-web
- homehub
- mqtt
- cctv
- ir-controller
- lock
- hvac
- lighting
- energy

Each service should eventually provide a Dockerfile, health check, minimal dependencies, non-root user where practical, deterministic seed/reset behavior, and a service README.

The root Compose definition will be added once service contracts are stable.
