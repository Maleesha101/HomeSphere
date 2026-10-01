# HomeSphere Agent / Builder Contract

## Mission

Build HomeSphere as a safe, reproducible, intentionally vulnerable smart-home ICS/IoT CTF.

## Core Rules

1. All vulnerabilities exist only in fictional lab components.
2. Never introduce real vendor credentials, real camera feeds, real Wi-Fi credentials, or real cloud tokens.
3. Do not implement functionality that controls physical devices.
4. Do not add wireless attack tooling or real credential-cracking workflows.
5. Keep inter-service communication inside the challenge network.
6. Prefer deterministic simulations over hardware.
7. Keep flags outside public player-facing source where practical.
8. Never commit production secrets, personal data, or credentials.
9. Every intended vulnerability needs a reset/recovery path.
10. Document intentional shortcuts for the author team.

## Architecture Principles

- Docker-first services
- Internal MQTT broker
- Resettable challenge state
- Explicit service contracts
- Per-team isolation where resources permit
- Reproducible seed data
- Minimal container privileges
- Health checks for runtime services

## Development Workflow

Use feature branches such as feature/web-portal, feature/android-app, feature/homehub, feature/cctv, feature/mqtt, and feature/ctfd.

Prefer small pull requests containing one subsystem or design change.

## Required Validation

- Docker build succeeds
- Service starts without Internet access
- Health check passes
- Reset procedure works
- No real secrets are present
- Intended solve path remains valid
- No unintended host/network escape is introduced
- Documentation matches implementation

Do not commit .env files, private keys, real credentials, real customer data, cloud API keys, or host SSH keys.
