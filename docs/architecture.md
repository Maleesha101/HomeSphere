# HomeSphere Architecture

HomeSphere models a residential automation environment as a small ICS-like control system.

## Logical Zones

1. Public Zone: vendor portal, documentation, download artifacts.
2. Application Zone: Android app, HomeHub API, CCTV portal.
3. Control Zone: MQTT broker, device simulators, event coordinator.
4. Device Zone: CCTV, smart lock, HVAC, lighting, energy meter, IR controller.

## Device Inventory

| Device | Function | Interface | Learning |
|---|---|---|---|
| HomeHub | Central automation | HTTP + MQTT | Architecture correlation |
| CCTV | Surveillance | HTTP + simulated stream | Misconfiguration analysis |
| Smart Lock | Access simulation | MQTT/API | Authorization assumptions |
| HVAC | Environmental control | MQTT | Telemetry reasoning |
| Lighting | Scene control | MQTT/API | State correlation |
| Energy Meter | Power telemetry | MQTT/log export | Timeline analysis |
| IR Controller | Legacy appliance bridge | HTTP/events | Protocol reasoning |

## Data Flow

Mobile App -> HomeHub/CCTV
Vendor Portal -> APK/Firmware
APK/Firmware -> HomeHub
HomeHub -> MQTT
MQTT -> CCTV, Lock, HVAC, Lighting, Energy, IR
Device events -> Event Correlator -> Final State

The player-facing network should expose only intended entry points. Device services and MQTT remain internal.
