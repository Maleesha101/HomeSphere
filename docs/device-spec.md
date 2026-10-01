# HomeSphere Device Specification

This is the initial device contract. Implementation details may evolve, but service boundaries and learning objectives should remain stable.

| ID | Device | Role | Primary Interface | Key Evidence |
|---|---|---|---|---|
| HUB-01 | HomeHub | Central coordinator | HTTP/MQTT | Event/state model |
| CAM-01 | CCTV | Surveillance | HTTP/simulated media | Camera metadata |
| LOCK-01 | Smart Lock | Access control simulation | MQTT/API | State transitions |
| HVAC-01 | HVAC | Environmental control | MQTT | Telemetry |
| LIGHT-01 | Lighting | Scene automation | MQTT/API | Scene state |
| ENERGY-01 | Energy Meter | Power telemetry | MQTT/logs | Timeline |
| IR-01 | IR Controller | Legacy appliance bridge | HTTP/events | Maintenance event |
| VOICE-01 | Voice/Scene Controller | Optional automation | MQTT | Easter egg/decoy |

## Device State Rules

Every simulator should expose a small, documented state model.

Every state transition must be:

- deterministic;
- resettable;
- observable through intended challenge evidence;
- unable to affect physical hardware.

## Protocol Rules

MQTT topics and payloads are fictional. Do not copy credentials or command formats from real commercial devices.
