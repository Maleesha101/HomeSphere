# HomeSphere Deployment Plan

## Recommended Environment

- Linux host or isolated VM
- Docker Engine and Docker Compose
- Optional CTFd instance
- Optional Android emulator
- No Internet requirement after images/assets are prepared

## Network Model

Create a dedicated Docker network for HomeSphere.

Player-facing services may publish selected ports to the CTF host. Internal services must not be published directly.

Suggested logical services:

- vendor-web: 8080
- homehub: 8081
- MQTT: 1883 internal
- CCTV: 8090
- IR simulator: 8091
- Node-RED: 1880 optional

## Deployment Checklist

- Build images locally or from trusted CTF infrastructure.
- Disable unnecessary outbound connectivity.
- Confirm internal services cannot reach the host.
- Use non-root containers where practical.
- Apply CPU/memory limits.
- Seed deterministic synthetic data.
- Verify health checks.
- Verify reset and flag validation.
- Snapshot the environment before an event.

## Reset Requirements

A reset must clear simulated device state, MQTT retained state, generated logs, challenge database state, and temporary player sessions while preserving challenge configuration.

## Safety Gate

Do not expose HomeSphere directly to the public Internet. For hosted CTFs, expose only the CTF gateway and keep device services behind the challenge network.
