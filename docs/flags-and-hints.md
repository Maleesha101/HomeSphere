# Flags and Progressive Hints

## Flag Design

Use synthetic flags such as flag{homesphere_<stage>_<random_suffix>}.

Do not commit live production flag values to public source-control branches when the repository is publicly visible.

## Planned Stages

| ID | Stage | Evidence |
|---|---|---|
| HS-01 | Recon | Vendor portal |
| HS-02 | Mobile | APK artifact |
| HS-03 | CCTV | Camera configuration/event |
| HS-04 | MQTT | Device message model |
| HS-05 | Control | Device-state correlation |
| HS-06 | IR | Maintenance event |
| HS-07 | Final | HomeHub state |

## Progressive Hints

Tier 1: "The smart home has more interfaces than the mobile app shows."

Tier 2: "The vendor documentation was written for developers, not attackers. Read what the developers left behind."

Tier 3: "The phone knows how the home is assembled. Inspect application resources and configuration."

Tier 4: "Cameras, locks, HVAC and lighting are not independent. Look for the message bus connecting them."

Tier 5: "The final controller validates a sequence of trusted device events. Reproduce the intended state inside the simulator."

Hints should reveal concepts rather than exact command sequences.
