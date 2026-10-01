# HomeSphere Safety Policy

HomeSphere is an educational simulation.

## Mandatory Controls

- Run inside an isolated CTF network.
- Use fictional device identities.
- Use synthetic credentials and tokens.
- Use simulated CCTV/video assets.
- Use simulated IR commands.
- Do not connect the challenge to real smart-home hardware.
- Do not use real Wi-Fi networks as targets.
- Do not expose MQTT or device-control services publicly.
- Do not use real vendor firmware or proprietary credentials.
- Do not grant containers host networking or unnecessary privileges.

## Release Hygiene

Before every release:

- scan for secrets;
- inspect Docker networking;
- verify no external callback URLs exist;
- verify media is fictional or licensed;
- verify flags are separated from public build artifacts where required.

## Player Notice

Players must be told that the environment is intentionally vulnerable and that testing must remain within the authorized CTF infrastructure.

## Incident Response

If an unintended escape or unsafe behavior is found: stop affected instances, isolate the host/network, preserve logs, patch the challenge, retest from a clean snapshot, and redeploy only after validation.
