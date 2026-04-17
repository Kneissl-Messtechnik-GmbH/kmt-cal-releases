# kmt-cal-releases

Öffentliches Distributionsrepository für signierte Release-Artefakte der **KMT Kalibriersoftware**.

## Was liegt hier?

- `latest.json` – Metadaten für den Tauri Auto-Updater (aktuelle Version, Downloadlinks, Signaturen)
- `releases/<version>/` – Signierte Installer-Artefakte pro Plattform

Der Quellcode liegt in einem **privaten** Repository. Dieses Repo enthält ausschließlich fertig gebaute, Ed25519-signierte Artefakte, die ausschließlich vom Tauri-Updater der installierten App konsumiert werden.

## Sicherheit

Jedes Release-Artefakt wird bei der Erstellung in GitHub Actions mit einem Ed25519-Key signiert. Der Tauri-Updater in der installierten App verifiziert die Signatur vor Installation gegen den in der App hinterlegten Public Key. Manipulierte Artefakte werden abgelehnt.

## Automatisch gepflegt

Inhalte dieses Repos werden ausschließlich vom CI-Workflow im Haupt-Repo geschrieben. Bitte nicht manuell committen.
