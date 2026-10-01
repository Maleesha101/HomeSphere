# HomeSphere — Smart Home ICS / IoT CTF

HomeSphere is a fully simulated smart-home security CTF for mobile reverse engineering, web reconnaissance, IoT protocol analysis, firmware analysis, CCTV misconfiguration discovery, and cross-device attack-chain reasoning.

Safety: HomeSphere is a fictional, intentionally vulnerable laboratory. Deploy it only inside an isolated CTF environment. No real cameras, smart-home devices, Wi-Fi credentials, cloud services, or vendor firmware are required.

## Scenario

HomeSphere's beta smart-home platform combines a mobile application, public product portal, central HomeHub, MQTT messaging, CCTV, smart locks, HVAC, lighting, energy monitoring, and IR-controlled appliances.

A rushed beta deployment left several development assumptions in production. Players correlate evidence across these components to demonstrate control of the simulated home and recover the final proof-of-compromise flag.

## Learning Areas

- Android application reconnaissance and reverse engineering
- Web/API reconnaissance
- IoT architecture and device fingerprinting
- MQTT concepts and topic analysis
- CCTV configuration analysis
- Firmware/configuration artifact analysis
- Event correlation and incident reasoning
- Safe ICS/IoT segmentation and defensive lessons

## High-Level Chain

Vendor Portal -> APK/Firmware -> HomeHub discovery -> CCTV/MQTT -> device state -> IR maintenance event -> HomeHub correlation -> final flag.

## Repository Structure

- AGENTS.md — builder/agent contract
- docs/ — challenge design and operational documentation
- docker/ — service packaging
- services/ — runtime implementations
- android/ — mobile application
- firmware/ — simulated firmware artifacts
- artifacts/ — synthetic PCAPs, logs, and media
- ctfd/ — scoring metadata/integration
- scripts/ — local build/reset/health scripts

## Status

Phase 0: challenge foundation. Runtime services and player artifacts will be added incrementally after the design is playtested.

See docs/safety.md before deployment.
