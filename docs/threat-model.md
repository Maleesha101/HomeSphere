# HomeSphere Threat Model

This is the threat model for a fictional challenge environment, not a real smart-home deployment.

## Assets

- HomeHub state
- Synthetic device identities
- Synthetic user/session data
- Challenge flags
- CTF scoring state

## Trust Boundaries

Player -> player-facing HTTP -> public services -> internal service network -> HomeHub/MQTT -> device simulators.

## Intended Weakness Categories

- Information exposure
- Authentication/authorization mistakes
- Insecure configuration
- Debug interfaces
- Weak device trust assumptions
- Event/state validation mistakes

## Out of Scope

- Real-world Wi-Fi exploitation
- Real camera compromise
- Physical lock bypass
- Bluetooth attacks against physical devices
- Cloud account takeover
- Malware
- Host persistence
- Arbitrary host command execution

## Defensive Lessons

The completed challenge should support a debrief on network segmentation, unique device credentials, secure mobile secret handling, MQTT authorization, camera access controls, firmware integrity, secure pairing, logging, and event validation.
