# HomeSphere Challenge Specification

## Identity

- Name: HomeSphere
- Theme: Smart-home ICS / IoT security
- Style: Multi-stage investigation and chained compromise simulation
- Target difficulty: Hard / Insane
- Audience: Intermediate-to-advanced CTF players
- Deployment: Docker/VM isolated laboratory

## Player Objective

Recover the final HomeSphere control flag by correlating evidence from the vendor portal, mobile application, simulated device services, network messaging, and device state.

## Intended Vulnerabilities

### Debug Artifact Exposure
Impact: Low/Medium. Difficulty: Easy.
Purpose: establish the ecosystem. Safe because all values are fictional.

### Mobile Configuration Leakage
Impact: Medium. Difficulty: Medium.
Purpose: teach inspection of application resources/configuration. Safe because values are synthetic.

### CCTV Misconfiguration
Impact: Medium. Difficulty: Easy/Medium.
Purpose: discover camera topology and event metadata. Safe because cameras and media are simulated.

### MQTT Authorization Weakness
Impact: Medium/High. Difficulty: Medium.
Purpose: teach event-driven IoT architecture. Safe because the broker is isolated.

### Device Debug State
Impact: Medium. Difficulty: Medium.
Purpose: connect application evidence to device state.

### IR Maintenance Logic
Impact: High within the lab. Difficulty: Hard.
Purpose: model insecure legacy-device integration. Safe because the controller accepts only predefined fictional commands.

### HomeHub Event Correlation
Impact: High within the lab. Difficulty: Hard.
Purpose: require multi-device reasoning rather than a single vulnerability.

## Intended Chain

Web recon -> APK/artifact discovery -> internal topology -> CCTV evidence -> MQTT/device mapping -> device-state conditions -> IR maintenance event -> HomeHub correlation -> final flag.

## Fairness

Every critical prerequisite should have at least two clues. Decoys must be distinguishable after reasonable validation. Final conditions must be deterministic and resettable.
