# Contributing to HomeSphere

## Branches

Use focused branches such as:

- feature/vendor-portal
- feature/android-app
- feature/homehub
- feature/cctv
- feature/mqtt
- feature/device-simulators
- feature/ctfd

## Pull Requests

Each PR should explain:

1. What changed?
2. Which challenge stage does it affect?
3. Which intended vulnerability or learning objective is involved?
4. How was it tested?
5. Does reset still work?
6. Does the change introduce any new network exposure?

## Security Review

Do not merge changes containing real credentials, real device integrations, host-network access, unnecessary privileged containers, or uncontrolled command execution.

## Testing

At minimum run:

build -> start -> health check -> intended solve path -> reset -> health check
