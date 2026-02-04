# Exigences produit (v0)

## Objectif
Livrer une application desktop installable sur PC qui permet :
- la détection et la configuration de cartes Arduino (Uno, Mega, etc.) et d’autres cartes compatibles ;
- la configuration de périphériques (moteurs pas‑à‑pas, encodeurs incrémentaux/rotatifs, entrées/sorties) ;
- la connexion et le mapping vers Microsoft Flight Simulator (MSFS) et X‑Plane.

## Cas d’usage principaux
1. **Détection automatique** : l’utilisateur branche une carte, l’app l’identifie et propose un profil.
2. **Configuration guidée** : l’utilisateur ajoute un encodeur ou un moteur pas‑à‑pas et choisit une action sim.
3. **Connexion simulateur** : l’utilisateur sélectionne MSFS ou X‑Plane et démarre la synchronisation.
4. **Diagnostic** : l’app affiche l’état des périphériques et des connexions.

## Exigences fonctionnelles
### Matériel
- Lister tous les ports série/USB disponibles.
- Identifier les cartes via VID/PID et signatures connues.
- Supporter un catalogue extensible (fichiers de définition).
- Permettre la configuration d’encodeurs (incrémentaux/rotatifs) et de moteurs pas‑à‑pas.

### Simulateurs
- Intégrer MSFS via SimConnect.
- Intégrer X‑Plane via UDP/SDK.
- Normaliser les actions via un “Sim Adapter” commun.

### UX
- Interface claire avec assistant de démarrage.
- Profils exportables/importables.
- Calibration et tests intégrés pour encodeurs et moteurs.

## Exigences non fonctionnelles
- Installation simple (packaging Windows en priorité).
- Logs et diagnostics exportables.
- Mise à jour possible du catalogue de cartes.

## Hors‑scope (v0)
- Support complet de toutes les cartes tierces dès la première version.
- Configuration avancée multi‑réseau.
