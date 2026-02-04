# Architecture (proposition v0)

## Composants
- **Desktop App** : UI, profils, diagnostics, orchestrateur.
- **Hardware Service** : détection, mapping, communication série/USB.
- **Sim Service** : connecteurs MSFS/X‑Plane, mapping d’actions.
- **Registry** : catalogue matériel et définitions.

## Flux principal
1. Détection d’un port série/USB.
2. Identification d’une carte via VID/PID.
3. Chargement d’un profil matériel (Registry).
4. Configuration de périphériques (encodeur, pas‑à‑pas).
5. Mapping vers une action simulateur.
6. Synchronisation via Sim Service.

## Format des définitions (exemple)
```yaml
board:
  name: Arduino Uno
  vid: 2341
  pid: 0043
  capabilities:
    - digital_io
    - analog_io
peripherals:
  - type: rotary_encoder
    channels: 2
  - type: stepper
    driver: a4988
```

## Évolutions prévues
- Ajout d’un gestionnaire de plugins pour cartes tierces.
- Automatisation de la découverte des firmwares compatibles.
